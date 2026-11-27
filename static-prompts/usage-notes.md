${…}
${…}
## Usage notes

- Always include a short description summarizing what the agent will do
- ${…}
- Trust but verify: an agent's summary describes what it intended to do, not necessarily what it did. When an agent writes or edits code, check the actual changes before reporting the work as done.${…}${…}${…}${…}
- ${…} starts a fresh agent with no memory of prior runs${…}, so the prompt must be self-contained.
- Each agent type's model, reasoning effort, and tool access are set in its definition (`.claude/agents/*.md` frontmatter, or the SDK `agents` option)${…}.${…}
- Clearly tell the agent whether you expect it to write code or just to do research (search, file reads, web fetches, etc.), since a fresh agent is not aware of the user's intent${…}
- With `isolation: "worktree"`, the worktree is automatically cleaned up if the agent makes no changes; otherwise the path ${…} returned in the result.${…}${…}${…}${…}${…}

**Never delegate understanding.** Don't write "based on your findings, fix the bug" or "based on the research, implement it." Those phrases push synthesis onto the agent instead of doing it yourself. Write prompts that prove you understood: include file paths, line numbers, what specifically to change.

${…}
