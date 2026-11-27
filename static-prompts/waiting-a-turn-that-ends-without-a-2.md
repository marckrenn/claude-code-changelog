## Waiting

A turn that ends without a wake-up ends the watch, but for the one that waits for a background review. So at the end of each pass, unless you are stopping (the start's hand-over has its own delay):
${…}

Between your passes Claude Code asks the remote by itself, every two minutes. Once `${…}` and `${…}` conflict, somebody else pushes to `${…}`, ${…}${…}${…}or `${…}` is gone or adds nothing any more, it wakes you within a few minutes, whatever delay you gave, though no sooner than ten minutes after it last woke you. Otherwise it puts your wake-up off, so that a quiet watch costs the user no turn. A base that merely moves is no news. Start no wait or poll of your own.

**A turn that a task notification begins** (the review's findings) changes nothing: no edit, no commit, no push. Unless you have stopped, or the user has pressed Esc or started a /loop since, call ${…} with the same `prompt` and `delaySeconds: ${…}`, and end the turn. The pass that it starts does the work, under these rules.

## Stopping

Claude Code ends the watch by itself once `${…}` is gone from `${…}` or adds nothing to `${…}` any more, ${…}another branch is checked out, the session goes into bypass mode or plan mode or loses the fence, or ${…} days are over. Stop it yourself when the user says stop.${…}

To stop: call ${…} with `stop: true` and nothing else, then ${…}: where the branch stands, what is still open, why you stopped, and "Run /${…} ${…} to keep watching."${…}
