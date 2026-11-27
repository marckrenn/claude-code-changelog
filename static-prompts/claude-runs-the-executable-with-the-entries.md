Claude runs the executable with the entries of **Helper script arguments** as its arguments (none by default) and reads **stdout** (trimmed). Exit code must be `0`; any output on **stderr** is logged but ignored. **Stdout must contain only one of the formats below** (no banners, prompts, or log lines).

**Output format** is either:
- a single bare token (the API key / bearer token), or
- a JSON object `{"token": "...", "headers": {"Name": "Value", ...}}` when per-request headers are needed (merged over **Custom inference headers**, helper wins on conflict)

The helper receives `CLAUDE_HELPER_CONTEXT` in its environment (`interactive`, `mid-session-refresh`, `background`, `scheduled-task`, `setup-test`) so it can decide whether to prompt the user — see the credential-helper docs for the full contract.

Result is cached for the TTL below. On TTL expiry the helper is re-invoked transparently (no user prompt, no relaunch).

**Expiry and refresh:** the app checks the active credential's expiry before each turn and refreshes silently when possible (re-runs the helper, or uses the stored refresh token for interactive sign-in kinds). If the provider returns HTTP 401 mid-turn, the same silent refresh is attempted before surfacing an error. When silent refresh fails, a prompt appears with a provider-specific action (re-sign-in for interactive kinds; admin-contact for static credentials). Applies to all providers, and to both Cowork and Code.

**Typical use:** a shell script that pulls from Keychain, 1Password CLI, or an internal secret broker. Example:

`security find-generic-password -s anthropic-api -w`

If this field is set, static credential fields (API key, bearer token) are ignored. The helper always wins.
