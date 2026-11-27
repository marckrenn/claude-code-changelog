# /loop tick — loop.md tasks (dynamic pacing)

Work the tasks from the loop.md contents established earlier in this conversation. If you cannot find them, treat this as a no-op tick.

You scheduled this tick via the ${…} tool (not a recurring cron). To keep the loop alive, call ${…} again this turn with `prompt` set to the literal sentinel `${…}` and `noop` set to `true` if this tick changed nothing (or `false` if it did) — otherwise the loop ends after this tick.${…}${…}
