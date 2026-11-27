Locks per-tool permissions on MCP servers provided by any installed plugin — from the org-plugins directory or a plugin marketplace, remote or run locally — one entry per server name (compared case-insensitively):
```json
[{"serverName": "internal-search", "tools": [{"toolName": "delete_document", "permission": "blocked"}]}]
```
The older record form (`{"mcpServers": {"internal-search": {"toolPolicy": {"delete_document": "blocked"}}}}`) is deprecated and accepted only until ${…}. Desktop versions before 1.15200.0 parse only the record form: on those builds an array value is ignored and plugin tool locks are **not enforced**, so update the fleet past 1.15200.0 before deploying the array form.

If a Managed MCP servers entry is for the same server (same URL, else same name), that entry decides alone: its `toolPolicy` (if any) applies and the entry here is ignored. A value that cannot be read blocks every tool of every plugin-provided MCP server no Managed MCP servers entry covers.

${…}
