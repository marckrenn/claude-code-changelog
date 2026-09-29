# Tool Description: file-pattern-matching-10

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${NUM}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_1}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_2}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

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
# Tool Description: file-pattern-matching-${EXPR_3}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_4}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_5}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_6}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_7}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching-${EXPR_8}

- Source: native-reference-match

## Summary

- Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
# Tool Description: file-pattern-matching

- Source: native-prompt-markdown-tool

## Summary

Fast file pattern matching tool that works with any codebase size - Supports glob patterns like "**/*.js" or "src/**/*.ts" - Returns matching file paths so…

# Raw Prompt Text
- Fast file pattern matching tool that works with any codebase size
- Supports glob patterns like "**/*.js" or "src/**/*.ts"
- Returns matching file paths sorted by modification time
- Use this tool when you need to find files by name patterns
- When you are doing an open ended search that may require multiple rounds of globbing and grepping, use the Agent tool instead
{
  "$schema": "${EXPR_9}
  "type": "object",
  "properties": {
    "pattern": {
      "description": "The glob pattern to match files against",
      "type": "string"
    },
    "path": {
      "description": "The directory to search in. If not specified, the current working directory will be used. IMPORTANT: Omit this field to use the default directory. DO NOT enter \"undefined\" or \"null\" - simply omit it for the default behavior. Must be a valid directory path if provided.",
      "type": "string"
    }
  },
  "required": [
    "pattern"
  ],
  "additionalProperties": false
}

---
