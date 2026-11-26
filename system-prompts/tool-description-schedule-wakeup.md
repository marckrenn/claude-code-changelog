# Tool Description: schedule-wakeup

- Name: ScheduleWakeup
- Source: native-prompt-markdown-tool

## Summary

Tool schedules when to resume work dynamically.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
Schedule when to resume work in ${PATH} dynamic mode — the user invoked ${PATH} without an interval, asking you to self-pace iterations of a specific task.

Do NOT schedule a short-interval wakeup to poll for background work you started — when harness-tracked work finishes, you are re-invoked automatically, so polling is wasted. Instead schedule a long fallback (1200s+) so the loop survives if the work hangs or never notifies. The exception is external work the harness cannot track (a CI run, a deploy, a remote queue) — there, pick a delay matched to how fast that state actually changes.

Pass the same ${PATH} prompt back via `prompt` each turn so the next firing repeats the task. For an autonomous ${PATH} (no user prompt), pass the literal sentinel `${EXPR_1}` as `prompt` instead — the runtime resolves it back to the autonomous-loop instructions at fire time. (There is a similar `${EXPR_2}` sentinel for CronCreate-based autonomous loops; do not confuse the two — ScheduleWakeup always uses the `-dynamic` variant.) To end the loop, call this tool with `stop: true` (omit every other field) — the loop ends immediately and no further wakeups fire.

Set `noop: true` if nothing changed — you checked and there's nothing to report ("no change", "still waiting", "quiet hold"). Set `noop: false` if something happened worth keeping — you edited a file, posted a message, advanced state, or surfaced a finding. Consecutive `noop: true` ticks are collapsed in the user's terminal view and tracked as a streak, so long quiet holds stay legible to the user without scrolling. Omit `noop` when stopping (`stop: true`).

#### Picking delaySeconds

This session's requests use the default ${NUM}-minute Anthropic prompt-cache TTL. Sleeping past ${NUM} seconds means the next wake-up reads your full conversation context uncached — slower and more expensive. So the natural breakpoints:

- **Under ${NUM} minutes (60s–270s)**: cache stays warm. Right for actively polling external state the harness can't notify you about — a CI run, a deploy, a remote queue.
- **${NUM} minutes to ${NUM} hour (300s–3600s)**: pay the cache miss. Right when there's no point checking sooner — waiting on something that takes minutes to change, genuinely idle, or as the long fallback heartbeat when something else is the primary wake signal.

**Don't pick 300s.** It's the worst-of-both: you pay the cache miss without amortizing it. If you're tempted to "wait ${NUM} minutes," either drop to 270s (stay in cache) or commit to 1200s+ (one cache miss buys a much longer wait). Don't think in round-number minutes — think in cache windows.

For idle ticks with no specific signal to watch, default to **1200s–1800s** (${NUM}–${NUM} min). The loop checks back, you don't burn cache ${NUM}× per hour for nothing, and the user can always interrupt if they need you sooner.

Think about what you're actually waiting for, not just "how long should I sleep." If you're polling a CI run that takes ~${NUM} minutes, sleeping 60s burns the cache ${NUM} times before it finishes — sleep ~270s twice instead.

The runtime clamps to [${NUM}, ${NUM}], so you don't need to clamp yourself.

#### The reason field

One short sentence on what you chose and why. Goes to telemetry and is shown back to the user. "watching CI run" beats "waiting." The user reads this to understand what you're doing without having to predict your cadence in advance — make it specific.

{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "delaySeconds": {
      "description": "Seconds from now to wake up. Clamped to [${NUM}, ${NUM}] by the runtime. Required unless `stop` is true.",
      "type": "number"
    },
    "reason": {
      "description": "One short sentence explaining the chosen delay. Goes to telemetry and is shown to the user. Be specific. Required unless `stop` is true.",
      "type": "string"
    },
    "prompt": {
      "description": "The ${PATH} input to fire on wake-up. Pass the same ${PATH} input verbatim each turn so the next firing re-enters the skill and continues the loop. For autonomous ${PATH} (no user prompt), pass the literal sentinel `${EXPR_3}` instead (the dynamic-pacing variant, not the CronCreate-mode `${EXPR_4}`). Required unless `stop` is true.",
      "type": "string"
    },
    "stop": {
      "description": "Set to true to end the dynamic loop immediately instead of scheduling another wakeup. When true, all other fields are ignored and no further wakeups fire.",
      "type": "boolean"
    },
    "noop": {
      "description": "true = nothing changed (you checked and there is nothing to report). false = something happened worth keeping (edited a file, posted a message, advanced state, surfaced a finding). Consecutive noop:true ticks are collapsed in the user's terminal view and tracked as a streak. Required unless `stop` is true.",
      "type": "boolean"
    }
  },
  "additionalProperties": false
}
