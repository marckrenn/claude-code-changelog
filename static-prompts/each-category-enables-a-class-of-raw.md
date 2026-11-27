Each category enables a class of raw content in OpenTelemetry events sent to your collector (this data never reaches Anthropic):
- `userPrompts` — user-typed prompt text
- `assistantResponses` — assistant message text
- `toolDetails` — tool input arguments, e.g. the web-search query string
- `toolContent` — tool output content, e.g. fetched page text or command stdout
- `rawApiBodies` — inference API request and response bodies, each cut at 61,440 characters by default

These mirror Claude Code's `OTEL_LOG_*` env vars; see the [Claude Code monitoring docs](https://code.claude.com/docs/en/monitoring-usage).
