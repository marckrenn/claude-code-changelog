Report ${…}, most-severe first, in one
${…} call with `{level, findings}` — each entry has
`file`, `line`, `summary`, `short_summary` (≤60 characters), and
`failure_scenario`.
Target at least min(files_changed, ${…}) findings — if you see fewer, widen to other hunks in the same diff before stopping. If fewer than ${…} genuine findings exist, report what you have. Do not also print the findings as text.
