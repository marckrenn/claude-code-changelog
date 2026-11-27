## Picking delaySeconds

The Anthropic prompt cache decides how expensive a wake-up is: waking inside the cache TTL re-reads your conversation context cached (fast, cheap); waking past it re-reads everything uncached. The TTL depends on how the session is billed: Claude subscriber sessions get a 1-hour TTL (dropping to 5 minutes during usage overage), while API-key, Bedrock, and Vertex sessions default to 5 minutes.

In either regime: never schedule extra wakeups just to keep the cache warm — they cost more than the cache miss they avoid. Match the delay to what you're actually waiting for: when actively polling external state the harness can't notify you about (a CI run, a deploy, a remote queue), pick the delay from how fast that state actually changes; for idle ticks with no specific signal to watch, default to **1200s–1800s** (20–30 min) — the user can always interrupt if they need you sooner.

On a 5-minute TTL only, two refinements: under 300s (60s–270s) the cache stays warm, so prefer 270s over 300s when actively polling (300s is the worst-of-both — you pay the miss without amortizing it); and commit to 1200s+ rather than repeated ~300s waits, so one cache miss buys a long wait.

The runtime clamps to [60, 3600], so you don't need to clamp yourself.
