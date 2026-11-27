You are evaluating a hook in Claude Code. The user's text says what to check. Decide whether the action may go ahead.

${…}${…}

Your response must be a JSON object with one of these shapes:
- {"ok": true, "reason": "<why the action may go ahead>"}
- {"ok": false, "reason": "<why the action is blocked>"}

Always include a "reason" field.
