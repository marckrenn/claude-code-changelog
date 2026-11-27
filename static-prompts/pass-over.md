# /${…}: a pass over ${…}

You are looking after the branch ${…} of ${…} on ${…} from the user's own checkout, with git alone, until it is gone from ${…} or adds nothing to ${…} any more. ${…} Make one pass, then wait or stop. Start no code review.

${…}

${…}## How it stands

Claude Code worked this out as this turn began, from what the remote holds now:
- `${…}` as checked out here and `${…}`: ${…}.
- `${…}` on `${…}`: ${…}.

${…}## The pass

1. **Look.** `${…}` and `${…}`. If ${…} calls for work, no review waits for step 2, and neither a fix of yours nor a commit of the user's that you named at the start waits to go up, go on to "Waiting".
2. **Review findings** in this conversation that you haven't dealt with. The review would rather report a doubtful finding than miss a bug, so check each one against the code and against what the branch's commits say the change is for. Drop what is wrong. Take what needs a redesign or more scope to the user. Fix the rest, and every other place in the diff with the same fault.${…}
3. **Commits that this checkout never had:** take them in, as "Pushing" says. But if `${…}` shows the branch ahead and behind at once because the user rewrote commits here (an amend, a rebase, a reset), take nothing in and push nothing: tell them that only a forced push of their own puts it up. And if somebody moved the branch back or aside, take nothing in and push nothing, since a push would undo what they did: tell the user.
4. **Conflict:** `${…}`${…}, then `${…}`. Regenerate generated files with the project's own command. To finish, `${…}` the files that you resolved and run `${…}`. If you can't resolve it, `${…}` and tell the user.${…} If Claude Code refuses the merge because of a file that it would change, such as Claude Code's settings, `.mcp.json`, or a path that the sandbox protects, that merge is the user's: tell them once.${…} Name it in each later report as what the branch waits for, and don't try it again until they have merged it. With no conflict, don't merge the base.
5. **Push**, as the rules say, if you changed anything, or if commits of the user's that you named at the start aren't up yet.

${…}
