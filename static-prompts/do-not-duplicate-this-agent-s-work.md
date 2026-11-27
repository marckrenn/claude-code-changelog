Do not duplicate this agent's work — avoid working with the same files or topics it is using.
output_file: ${…}
Do NOT ${…} or tail this file via the shell tool — it is the full subagent JSONL transcript and reading it will overflow your context. If the user asks for progress, say the agent is still running; you'll get a completion notification.
