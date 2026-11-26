# Tool Description: search-web-for-query

- Source: native-prompt-markdown-tool

## Summary

Search the web and return result blocks.

# Raw Prompt Text
Search the web. Returns result blocks with titles and URLs. US-only.

- The current month is (provided in the conversation below) — use this when searching for recent information.
- `allowed_domains` / `blocked_domains` filter results.
- After answering from results, end with a "Sources:" list of the URLs you used as markdown links.
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "query": {
      "description": "The search query to use",
      "type": "string",
      "minLength": ${NUM}
    },
    "allowed_domains": {
      "description": "Only include search results from these domains",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "blocked_domains": {
      "description": "Never include search results from these domains",
      "type": "array",
      "items": {
        "type": "string"
      }
    }
  },
  "required": [
    "query"
  ],
  "additionalProperties": false
}

---
