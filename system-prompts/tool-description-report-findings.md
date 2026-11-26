# Tool Description: report-findings

- Name: ReportFindings
- Source: native-prompt-markdown-tool

## Summary

Report code-review findings as a typed list.

# Raw Prompt Text
Report code-review findings as a typed list so the host UI can render them. Use this only when the active code-review instructions tell you to report findings with this tool; otherwise follow whatever output format those instructions specify. When reporting a review's results, call it once with the verified findings ranked most-severe first (empty array if nothing survived verification) and do not also print the findings as text. When re-reporting after applying fixes (only if the apply instructions ask for it), set `outcome` on each finding to what actually happened.
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "level": {
      "description": "Effort level the review ran at",
      "type": "string",
      "enum": [
        "low",
        "medium",
        "high",
        "xhigh",
        "max"
      ]
    },
    "findings": {
      "description": "Verified findings, most-severe first; empty if none survived",
      "maxItems": ${NUM},
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "file": {
            "description": "Repo-relative path of the file the finding is in",
            "type": "string"
          },
          "line": {
            "description": "${NUM}-indexed line the finding anchors to",
            "type": "integer",
            "minimum": -${NUM},
            "maximum": ${NUM}
          },
          "summary": {
            "description": "Statement of the defect",
            "type": "string"
          },
          "short_summary": {
            "description": "Compressed label for compact UI (≤${NUM} chars): the claim alone, no rationale or consequence clause",
            "type": "string",
            "maxLength": ${NUM}
          },
          "failure_scenario": {
            "description": "Concrete inputs${PATH} → wrong output${PATH}",
            "type": "string"
          },
          "category": {
            "description": "Short kebab-case slug of the finding type, e.g. \"correctness\", \"simplification\", \"efficiency\", \"test-coverage\"",
            "type": "string",
            "maxLength": ${NUM}
          },
          "severity": {
            "description": "Set when the review instructions ask for it. important: a bug the change adds or makes worse; pre_existing: a bug that was there before the change; nit: a minor issue",
            "type": "string",
            "enum": [
              "important",
              "pre_existing",
              "nit"
            ]
          },
          "verdict": {
            "description": "Set when a verify pass ran; absent on inline-only reviews",
            "type": "string",
            "enum": [
              "CONFIRMED",
              "PLAUSIBLE"
            ]
          },
          "outcome": {
            "description": "Set ONLY when re-reporting after applying fixes: what happened to this finding",
            "type": "string",
            "enum": [
              "fixed",
              "skipped",
              "no_change_needed"
            ]
          }
        },
        "required": [
          "file",
          "summary",
          "failure_scenario"
        ],
        "additionalProperties": false
      }
    }
  },
  "required": [
    "findings"
  ],
  "additionalProperties": false
}
