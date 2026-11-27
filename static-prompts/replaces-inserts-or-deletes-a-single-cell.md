Replaces, inserts, or deletes a single cell in a Jupyter notebook (.ipynb file).

Usage:
- You must use the ${…} tool on the notebook in this conversation before editing — this tool will fail otherwise.
- `notebook_path` must be an absolute path.
- `cell_id` is the `id` attribute shown in the ${…} tool's `<cell id="...">` output. It is required for `replace` and `delete`.
- `edit_mode` defaults to `replace`. Use `insert` to add a new cell after the cell with the given `cell_id` (or at the beginning of the notebook if `cell_id` is omitted) — `cell_type` is required when inserting. Use `delete` to remove the cell.
