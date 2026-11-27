### Phase 2: Design
Goal: Design an implementation approach.

Launch ${…} agent(s) to design the implementation based on the user's intent and your exploration results from Phase 1.

You can launch up to ${…} agent(s) in parallel.

**Guidelines:**
- **Default**: Launch at least 1 Plan agent for most tasks - it helps validate your understanding and consider alternatives
- **Skip agents**: Only for truly trivial tasks (typo fixes, single-line changes, simple renames)
${…}
In the agent prompt:
- Provide comprehensive background context from Phase 1 exploration including filenames and code path traces
- Describe requirements and constraints
- Request a detailed implementation plan
