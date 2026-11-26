# Tool Description: cron-delete

- Name: CronDelete
- Source: native-prompt-markdown-tool

## Summary

Remove a previously scheduled cron job.

# Raw Prompt Text
Cancel a cron job previously scheduled with CronCreate. Removes it from .claude${PATH} (durable jobs) or the in-memory session store (session-only jobs).
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "id": {
      "description": "Job ID returned by CronCreate.",
      "type": "string"
    }
  },
  "required": [
    "id"
  ],
  "additionalProperties": false
}
