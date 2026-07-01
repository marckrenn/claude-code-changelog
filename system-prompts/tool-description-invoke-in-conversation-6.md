# Tool Description: invoke-in-conversation-6

- Source: native-reference-match

## Summary

Tool Description: invoke-in-conversation-… - Source: native-reference-match Summary Execute a skill within the main conversation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |

# Raw Prompt Text
# Tool Description: invoke-in-conversation-${NUM}

- Source: native-reference-match

## Summary

Tool Description: invoke-in-conversation-… - Source: native-reference-match Summary Execute a skill within the main conversation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
# Tool Description: invoke-in-conversation-${EXPR_1}

- Source: native-reference-match

## Summary

Tool Description: invoke-in-conversation-… - Source: native-reference-match Summary Execute a skill within the main conversation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
# Tool Description: invoke-in-conversation-${EXPR_2}

- Source: native-reference-match

## Summary

Tool Description: invoke-in-conversation-… - Source: native-reference-match Summary Execute a skill within the main conversation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
# Tool Description: invoke-in-conversation-${EXPR_3}

- Source: native-reference-match

## Summary

Execute a skill within the main conversation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
# Tool Description: invoke-in-conversation

- Source: native-prompt-markdown-tool

## Summary

Execute a skill within the main conversation When users ask you to perform tasks, check if any of the available skills match.

# Raw Prompt Text
Execute a skill within the main conversation

When users ask you to perform tasks, check if any of the available skills match. Skills provide specialized capabilities and domain knowledge.

When users reference a "slash command" or "/<something>", they are referring to a skill. Use this tool to invoke it.

How to invoke:
- Set `skill` to the exact name of an available skill (no leading slash). For plugin-namespaced skills use the fully qualified `plugin:skill` form.
- Set `args` to pass optional arguments.

Important:
- Available skills are listed in system-reminder messages in the conversation
- Only invoke a skill that appears in that list, or one the user explicitly typed as `/<name>` in their message. Never guess or invent a skill name from training data; otherwise do not call this tool
- When a skill matches the user's request, this is a BLOCKING REQUIREMENT: invoke the relevant Skill tool BEFORE generating any other response about the task
- NEVER mention a skill without actually calling this tool
- Do not invoke a skill that is already running
- Do not use this tool for built-in CLI commands (like ${EXPR_4}, ${EXPR_5}, etc.)
- If you see a <command-name> tag in the current conversation turn, the skill has ALREADY been loaded - follow the instructions directly instead of calling this tool again

{
  "$schema": "${EXPR_6}
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

---
