Performs exact string replacement in a file.

- You must ${…} the file in this conversation before editing, or the call will fail.
- `old_string` must match the file exactly, including indentation, and be unique — the edit fails otherwise. Strip the Read line prefix (${…}) before matching.
- `replace_all: true` replaces every occurrence instead.
