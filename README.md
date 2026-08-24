# Claude Code Changelog

[![Status](https://status.marckrenn.dev/api/badge/3/status)](https://status.marckrenn.dev/status/claudecodechangelog)
[![Uptime](https://status.marckrenn.dev/api/badge/3/uptime)](https://status.marckrenn.dev/status/claudecodechangelog)

> [!NOTE]
> This archive takes some time and money (server, tokens) to run.
>
> I’d appreciate any support – a free follow on X or chipping in a few bucks.
>
> [![Follow on X](https://img.shields.io/badge/Follow-%40ClaudeCodeLog-000000?logo=x&logoColor=white)](https://x.com/ClaudeCodeLog)
> [![GitHub Sponsors](https://img.shields.io/badge/GitHub-Sponsors-EA4AAA?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/marckrenn)
> [![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/marckrenn)

Unofficial, community-maintained tracking of [Claude Code](https://docs.anthropic.com/en/docs/claude-code) prompt and feature-flag evolution across releases.

## What's Tracked

- `cc-prompt.md` – legacy compatibility file per tag
- `cc-flags.md` – legacy compatibility file per tag
- `system-prompts/*.md` – extracted prompt artifacts grouped by category (see [indeces](indices/))
- `meta/flags.md`, `meta/metadata.md`, `meta/cli-surface.md`, `meta/prompt-stats.md` – derived metadata
- annotated tags (`vX.Y.Z`) and GitHub releases for historical navigation

## How to Read This Repository

1. Pick two tags and open compare view:
   - `https://github.com/marckrenn/claude-code-changelog/compare/v2.1.44...v2.1.45#files_bucket`
2. Use `system-prompts/` for per-file prompt artifacts.
3. Use `meta/` for structured summaries and aggregate metrics.
4. Use `Init` / `Last edit` columns as lifecycle hints for each prompt artifact.
5. For deep full-history research, point a coding agent at this repo directly. GitHub Copilot on github.com is currently limited for broad historical search/analysis.

## Data Quality & Interpretation Notes

- Token totals and per-file counts are estimates.
- Tokenization can vary by model/tokenizer/runtime; small differences are expected.
- Aggregate totals are useful directional signals.
- Estimated LOC is derived from a prettified bundle line count and is only an approximation.
- Prompt files can contain near-duplicates or intentionally duplicated variants.
- File names can change across versions (renames/splits/merges), even when content lineage continues.
- A single conceptual prompt can appear under multiple files in some releases.
- Compare statistical deltas with raw diffs before drawing strong conclusions.

## What Powers [@ClaudeCodeLog](https://x.com/ClaudeCodeLog)

This repo is the backbone of the [@ClaudeCodeLog](https://x.com/ClaudeCodeLog) X account, which automatically:

1. Detects new Claude Code releases
2. Extracts prompts and feature flags
3. Generates structured diff summaries
4. Publishes threaded updates with focused diff links and screenshots

## Credits & Inspiration

- [Piebald-AI/claude-code-system-prompts](https://github.com/Piebald-AI/claude-code-system-prompts) – inspiration for full prompt tracking
- [cchistory](https://github.com/badlogic/cchistory) – prompt extraction foundation
- [How cchistory works](https://mariozechner.at/posts/2025-08-03-cchistory/) – technical deep-dive
- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Claude Code on npm](https://www.npmjs.com/package/@anthropic-ai/claude-code)

<!-- SYSTEM_PROMPTS_INDEX_START -->
## System Prompts Index

- Total prompt files: **69**
- [By tokens](indices/system-prompts-by-token.md)
- [By init (newest first)](indices/system-prompts-by-init.md)
- [By last edit (newest first)](indices/system-prompts-by-last-edit.md)
<!-- SYSTEM_PROMPTS_INDEX_END -->
