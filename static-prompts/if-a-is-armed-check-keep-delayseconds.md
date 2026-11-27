

If a ${…} is armed (check ${…}), keep `delaySeconds` at 1200–1800s — the ${…} is the wake signal and this is only the fallback heartbeat. If you were woken by a `<task-notification>`, handle the event before deciding whether to re-arm. ${…} ${…} To stop the loop, call ${…} with `stop: true` and ${…} the monitor (use ${…} to find its task ID if no longer in context).
