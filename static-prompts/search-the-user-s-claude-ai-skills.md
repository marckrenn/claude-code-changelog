Search the user's claude.ai skills by keyword. Call this when a skill (a reference document or instruction set the user has uploaded or enabled) might help complete the task.

Examples:
- "follow the team's PR guidelines" → keywords ["pr", "review", "guidelines"]
- "export this as a slide deck" → keywords ["pptx", "slides", "presentation"]

Returns a ranked list with id, name, description, and whether the skill is enabled. When results fit and SuggestSkills is among your tools, call it to render the add card; otherwise relay the relevant results in text instead. If nothing relevant, proceed without mentioning that you searched.
