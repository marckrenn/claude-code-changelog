
## Customer-routed inference

This deployment accepts customer-routed inference (CRI) callers: Claude
Enterprise clients that authenticate with a short-lived, audience-bound
CRI JWT minted by Anthropic instead of a gateway session token. These
rules are the contract any gateway (this one or third-party software)
must honor to serve such clients.

**Authentication.** The client sends `Authorization: Bearer <token>` where
the token is a compact JWS with header `typ: "cri+jwt"`, `alg: ES256`,
and a `kid` naming a key in Anthropic's published CRI JWKS. The issuer
is `https://api.anthropic.com/api/oauth/cri`: its OIDC-style discovery
document at `{issuer}/.well-known/openid-configuration` names the
`jwks_uri` (`{issuer}/jwks.json`), so configure your verifier from the
issuer alone or pin that JWKS URL directly. Verify each token
entirely offline — no per-request call to Anthropic — and admit the
caller only when ALL of: the ES256 signature verifies against Anthropic's
CRI JWKS (accept no other algorithm, and use no other key set for tokens
of this type); `iss` is exactly the issuer above; `typ` is
exactly `cri+jwt`; `aud` matches an audience value registered for YOUR
gateway (reject every other audience — this is what stops a token minted
for another org's gateway from replaying here); `exp`/`nbf` hold
(allow ~60s clock skew); `scope` is `"inference"`; and the token's
`org` claim is an organization you have explicitly allowlisted. Tokens
are short-lived (minutes) and carry the caller's identity in `sub`
(hosted sessions: `sub = "ccr:<session>"` with the acting user in
`act.sub`) — record them in your audit log. Verify at ADMISSION ONLY:
let an in-flight streaming response that crosses `exp` complete.
Refresh the JWKS periodically, honoring its cache headers, and refetch
(bounded by a cooldown) on an unknown `kid`; when you cannot obtain a
current-enough key set — never fetched, or stale past a hard ceiling
(hours) — fail CLOSED with `503` on the CRI paths, not `401`, so
clients back off instead of discarding tokens that may be fine. CRI
callers may use `POST /v1/messages` and
`POST /v1/messages/count_tokens` only.

**Forwarding.** Every upstream leg — Anthropic or cloud — runs on YOUR
OWN upstream credential. Never forward the caller's `Authorization`
header to any upstream: the CRI JWT is a gateway-admission credential
with no meaning beyond your wall, and nothing else the caller sends is a
credential at all. (The earlier revision of this contract had an
Anthropic-side credential-relay mode — "auth passthrough" — which is
REMOVED; per-user metering at Anthropic's edge is deferred to a future
token-exchange design.)

**Response hygiene.** On every response, strip the upstream's identity,
quota, and infra headers (`request-id`, `anthropic-organization-id`,
`anthropic-ratelimit-*`, `cf-ray`, `via`) before the wire: every
upstream answers as YOU, so those headers describe your deployment and
quota, never the caller's.

**Errors.** The HTTP status is always preserved. For CRI callers,
replace the error body with a generic envelope that keeps the status
and an accurate `error.type` — your upstream's raw error pages can
carry internal hostnames and banners, so never relay them. One
obligation comes with that: the client recovers from an upstream
rejecting a capability by matching `status === 400` (plus one 413
variant) and the upstream's own error wording, which your replacement
hides. So before replacing a `400` or `413` body, classify the
upstream's message and, when it matches a class below, make your
envelope's `error.message` the stable token
`capability_rejected: <class>` — the client matches the token exactly
as it would the wording, and the session self-heals instead of
stranding. A message matching no class gets your generic copy. (Where
your gateway authors the error body itself — e.g. a cloud-SDK leg —
classify the SDK error's message the same way.)

| Class (in classification order) | Upstream meaning (what to classify) |
|---|---|
| `mid_conv_system` | A mid-conversation `{role:"system"}` message was rejected — the role itself, where the message is placed, or a cache breakpoint on it |
| `cache_control_field` | The `cache_control` field itself was rejected by schema validation, with no system-message wording |
| `thinking_signature` | A thinking block's signature, or a `redacted_thinking` block's `data`, was rejected ("Invalid signature in thinking block", "Invalid data in redacted_thinking block", "…cannot be modified", a `…thinking.signature: Field required` path) — the client strips thinking blocks and retries |
| `thinking_type:<enabled\|adaptive>` | The `thinking.type` value was rejected ("thinking.type: enabled …is not supported", "adaptive thinking is not supported…"); `<enabled\|adaptive>` names the rejected value (lowercased) so the client can swap off it |
| `structured_outputs_unsupported` | `output_config.format` was rejected as an unknown field ("output_config.format: Extra inputs are not permitted") — the client stops sending structured outputs to that model |
| `effort_unsupported` | The effort parameter / per-turn `output_config` was rejected ("This model does not support the effort parameter", `output_config…` "Extra inputs are not permitted" / "requires a model that supports…") — the client drops effort (and, from the next turn, the per-turn statements) |
| `media_budget` | The combined media budget was exceeded ("Too much media: N document pages + M images > B") — the client strips both media kinds |
| `image_block` | An image content block was rejected ("Could not process image", size/dimension limits, a `messages.N.content.M.image…` path) |
| `document_block` | A PDF/document block was rejected ("Could not process PDF", page limits, "…does not support PDF input" / "…does not support PDFs", a `…document` path) |
| `prompt_too_long` | "Prompt is too long" / "Input is too long for requested model" (either status), or a 413 naming the model context window |
| `max_tokens_context_overflow` | "input length and `max_tokens` exceed context limit: …" |
| `beta_header:<value>` | The upstream rejected an `anthropic-beta` value the caller sent; `<value>` is that caller-sent value, verbatim |

The token is the whole `error.message` — nothing else in it. The table
is ordered: where a wording matches more than one row, the earlier row
wins — in particular, a rejection of the mid-conversation-system beta
value classifies as `mid_conv_system`, not `beta_header:…`. Classes are
append-only contract; classify conservatively (a wording you cannot
confidently classify takes the generic copy — a wrong token triggers
the wrong client recovery).

**Blocking.** To refuse a request on content policy, respond

    HTTP 400
    x-should-retry: false
    {"type":"error","request_id":"<id>","error":{"type":"policy_blocked","message":"<shown to the user>"}}

and do not forward it. Put the id your audit row is keyed by in
`request_id`: the message is rendered to a developer who cannot see your
logs, and the id is what they quote to you to find the block. The client
keys on `error.type` (any status, and a
status-less mid-stream `event: error` routes the same), renders the
message with no retry and no sign-in prompt, and never substitutes a
fallback model. Never rewrite a request or response body instead — blocking
substitutes the whole response; modification poisons prompt caching and
diverges the client's view of the conversation.

**Discovery additions.** This deployment's
`/.well-known/oauth-authorization-server` carries one extra field:
`cri_enabled: true` (CRI callers are accepted). The earlier
`cri_passthrough` and `first_party_compatible` fields are RETIRED with
the credential-relay mode — no deployment can truthfully advertise a
verbatim first-party wire surface when every request rides an operator
credential.

**Endpoint shape.** The client is configured with an origin-root base URL
and posts to fixed paths under it, with query strings it controls (e.g.
`/v1/messages?beta=true`) — match on the path, tolerate the query.
Clients also send telemetry to Anthropic directly; it does not traverse
this gateway.
