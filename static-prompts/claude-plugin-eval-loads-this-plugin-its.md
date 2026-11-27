
`claude plugin eval` loads this plugin (its skills, hooks and MCP servers) and runs its eval suite - prompts and graders; scaffold scripts only with --scaffold - on this machine, as you. The run is sandboxed where the platform supports it, which limits what a malicious plugin can reach but is not a guarantee against one. A plugin's own suite passing says nothing about whether the plugin is safe.
  Plugin directory: ${…}
${…}Only evaluate plugins you trust.
