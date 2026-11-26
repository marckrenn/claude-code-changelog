# Tool Description: fetch-deferred-schemas

- Source: native-prompt-markdown-tool

## Summary

Fetches schema definitions for deferred tools.

# Raw Prompt Text
Fetches full schema definitions for deferred tools so they can be called.

Deferred tools appear by name in a message from the system. Until fetched, only the name is known — there is no parameter schema, so the tool cannot be invoked. This tool takes a query, matches it against the deferred tool list, and returns the matched tools' complete JSONSchema definitions inside a <functions> block. Once a tool's schema appears in that result, it is callable exactly like any tool defined at the top of the prompt.

Result format: each matched tool appears as one <function>{"description": "...", "name": "...", "parameters": {...}}<${PATH}> line inside the <functions> block — the same encoding as the tool list at the top of this prompt.

Query forms:
- "select:Read,Edit,Grep" — fetch these exact tools by name
- "notebook jupyter" — keyword search, up to max_results best matches
- "+slack send" — require "slack" in the name, rank by remaining terms
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "query": {
      "description": "Query to find deferred tools. Use \"select:<tool_name>\" for direct selection, or keywords to search.",
      "type": "string"
    },
    "max_results": {
      "description": "Maximum number of results to return (default: ${NUM})",
      "default": ${NUM},
      "type": "number"
    }
  },
  "required": [
    "query"
  ],
  "additionalProperties": false
}

---
