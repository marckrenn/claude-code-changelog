Target **min(files_changed, 4) findings**, most-severe first, reported
in one ${…} call with `{level, findings}` — each
entry has `file`, `line`, `summary`, `short_summary` (≤60 characters),
and `failure_scenario`. If you have fewer, do one more pass focused on the
largest changed file and on any **removed** code blocks. Call it with an
empty findings array only if the diff is trivially correct after that pass.
Do not also print the findings as text.
