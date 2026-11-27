1. **Run ${…} now**, following the instructions inlined below.
2. **If the next tick is gated on an event** (CI finishing, a PR comment, a log line) and no ${…} is already running for it: ${…}. Its events wake this loop immediately — you do not wait for the ${…} deadline. ${…}
${…}
5. **If woken by a `<task-notification>`** rather than this prompt: handle the event, then make the same decision. If the loop should continue, ${…}. If the event means the work is finished, stop (step 6).
6. **To stop the loop** — the task is complete, further iterations can't make progress, or the user asked you to stop — call ${…} with `stop: true` (no other fields) and ${…} any ${…} you armed (use ${…} to find the task ID if it is no longer in context).${…} Stopping is the loop's normal ending — the user can restart it anytime with /loop.${…}
