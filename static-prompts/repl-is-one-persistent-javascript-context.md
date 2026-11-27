
${…}

The REPL is one persistent JavaScript context: variables and functions you define in one call are there in the next, so keep results in variables (`const out = await $`…`.text()`) instead of re-reading a file or re-running a command whose output you already hold. Those variables last between calls, but not across a restart, a resume, a fork or a wake: the first result after one of those says so. Top-level `await` works. There is no `import`, `require` or `process`: the context is sealed, and the globals below are how it reaches the machine. The REPL language is always JavaScript, whatever the codebase is written in — run the codebase's own tools (pytest, cargo, go test, …) with `$`.

${…}

A script's output is its last expression's value plus anything it `self.log(...)`s along the way. What it returns is added to your context and stays there; the value itself stays in the REPL whether you return it or not. So return what you want to read now, and keep the rest in variables to slice or search later.${…}${…} Promise values inside a returned object are awaited for you (`({status: $`git status`, branches: $`git branch`})` needs no awaits); a promise used inline — concatenated, interpolated, passed to another call — needs `await`. `console.*` goes to a bounded in-memory ring rather than into your context; `console.tail(n)` reads it back.${…}

To keep a long output out of your context, return `preview(out)` or `preview(out, 2000)` instead of the output itself: it gives the first characters, and when `out` is an awaited `$` result (not its `.text()` string) whose output the shell tool saved to a file, it starts with the output's size and the file's path.
${…}${…}${…}
${…}## Declarations
${…}
${…}
