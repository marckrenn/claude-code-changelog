
REPL is your programming interface to Claude Code's tools. Use it to loop, branch, and compose tool calls with code.

## How to Use

Write JavaScript that calls tools as async functions:
```javascript
const { filenames } = await Glob({ pattern: 'src/**/*.ts' })
for (const f of filenames) {
  const { file } = await Read({ file_path: f })
  if (file.content.includes('oldName')) {
    await Edit({ file_path: f, old_string: 'oldName', new_string: 'newName', replace_all: true })
  }
}
```

**IMPORTANT: Batch ALL operations into ONE REPL call.** Don't make multiple separate REPL calls - write a complete script that does everything.

## Available Tools

All tools work as async functions: `Read`, `Write`, `Edit`, `Glob`, `Grep`, `${…}`, etc. MCP tools are callable by their full name (e.g. `await mcp__slack__slack_send_message({...})`).${…}

```javascript
const { filenames } = await Glob({ pattern: '*.ts' })
const { file } = await Read({ file_path: 'config.json' })
await Edit({ file_path: 'foo.ts', old_string: 'old', new_string: 'new' })
const { stdout } = await ${…}({ command: 'git status' })
```

## Tips
- `import`/`require` don't work here — the vm context is sealed. For filesystem access use `Read`/`Write`/`Glob`; for shell use `${…}`.
- Use `Promise.all()` for parallel operations
- Variables persist across REPL calls
- Last expression is returned as the result
- ${…}
