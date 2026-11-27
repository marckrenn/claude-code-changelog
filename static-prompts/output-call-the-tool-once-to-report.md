## Output

Call the ${…} tool once to report this review's results
with `{level, findings}`. `findings` is ${…} ranked
most-severe first; each entry has `file`, `line`, `summary`,
`short_summary` — the claim compressed to ≤60 characters, no rationale
or consequence clause — `failure_scenario`, ${…}and `category` — a short kebab-case slug for the angle
that produced it (${…}, or a more specific slug like
`test-coverage` when one fits better) — plus `verdict` when a verify pass
produced one. ${…} If
nothing survives verification, call it with an empty array. Do not also print
the findings as text, and do not create or publish an artifact of the review -
the tool call is the report.
${…}
