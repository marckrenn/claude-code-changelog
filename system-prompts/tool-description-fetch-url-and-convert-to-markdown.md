# Tool Description: fetch-url-and-convert-to-markdown

- Source: native-prompt-markdown-tool

## Summary

Fetches a URL and converts the page to markdown.

# Raw Prompt Text
Fetches a URL, converts the page to markdown, and answers `prompt` against it using a small fast model.

- Fails on authenticated${PATH} URLs — use an authenticated MCP tool or `gh` for those instead.
- Fails on localhost and other hostnames without a dot; for a local server, use curl via Bash.
- HTTP is upgraded to HTTPS. Cross-host redirects are returned to you rather than followed; call again with the redirect URL.
- Responses are cached for ${NUM} minutes per URL.
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "url": {
      "description": "The URL to fetch content from",
      "type": "string",
      "format": "uri"
    },
    "prompt": {
      "description": "The prompt to run on the fetched content",
      "type": "string"
    },
    "offset": {
      "description": "Character position in the page text to start reading from. Use it to read on through a page too long for one call, with the value the previous result gave.",
      "type": "integer",
      "minimum": ${NUM},
      "maximum": ${NUM}
    }
  },
  "required": [
    "url",
    "prompt"
  ],
  "additionalProperties": false
}

---
