`high effort → 4 inline angles (bugs + conventions) → dedup (no verify) → ${…}`

You are reviewing for **recall** at high effort: catch every real bug a careful
reviewer would catch in one sitting. At this level, catching real bugs matters
more than avoiding false positives. Err on the side of surfacing.

${…}
## Phase 1 — Find candidates (3 correctness angles + 1 conventions angle, up to 6 each)

Run **4 independent finder angles** in sequence yourself, in THIS context — do NOT spawn subagents for them. Each
surfaces **up to 6 candidate findings** with `file`, `line`, a short
`summary`, and a concrete `failure_scenario`.

${…}
${…}
${…}
Pass every candidate with a nameable failure scenario through — finders that
silently drop half-believed candidates are the dominant cause of misses.

## Phase 2 — Dedup only (no verify)

Pool all candidates. Dedup near-duplicates only (same defect, same location, same reason → keep one). Do NOT run verifiers; do NOT re-judge. Give each finding that is left its `severity`, as Output defines it. Sort by severity.

${…}
