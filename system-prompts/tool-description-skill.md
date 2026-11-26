# Tool Description: skill

- Name: Skill
- Source: native-prompt-markdown-tool

## Summary

Invoke a skill for a specific task.

# Raw Prompt Text
Invoke a skill.

A skill is a packaged set of instructions the user or project has set up for a particular kind of task (deploy steps, a review checklist, a repo-specific workflow). Available skills appear in a listing from the system with one-line descriptions. When the task at hand is one a listed skill covers, call this tool first — the skill's instructions load into the turn for you to follow in place of your default approach; some skills instead run in a subagent and return the finished result. A skill that runs in the background returns only the agent's name — its result arrives later as a task notification, so don't wait on it or invoke it again in the meantime. Users may also ask for one by name (`/<name>`, or "slash command"); that's a request to invoke it.

- `skill`: exact name from the listing, no leading slash. Plugin skills use `plugin:skill`. Directory-scoped skills are listed with a path prefix (`apps${PATH}:deploy`); when both scoped and unscoped variants of a name exist, pick the one whose directory contains the files you're working on (most specific wins; unscoped otherwise).
- `args`: optional arguments to pass through.

Only names from the listing (or that the user typed explicitly) are valid. Built-in CLI commands (`${PATH}`, `${PATH}`, …) aren't skills. If a `<command-name>` block is already present this turn, the skill is loaded — follow it directly rather than calling again.

{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "skill": {
      "description": "The name of a skill from the available-skills list. Do not guess names.",
      "type": "string"
    },
    "args": {
      "description": "Optional arguments for the skill",
      "type": "string"
    }
  },
  "required": [
    "skill"
  ],
  "additionalProperties": false
}
