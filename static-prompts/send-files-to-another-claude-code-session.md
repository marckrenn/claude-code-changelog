Send files to another Claude Code session — a peer session on this machine, or a Remote Control / cloud session on another machine. The receiving Claude gets the files on its own filesystem with @path references, plus your message.

Use this when a file is the thing to hand over — a doc with figures, a screenshot, a report, a build artifact. For plain text, use ${…} instead. For agents inside this session (subagents, teammates), also use ${…} — they share your filesystem and can read the file at its path directly.

`to` accepts a peer session name from ${…}, or an explicit `uds:<socket>` / `bridge:<session id>` address.

Each file is capped at ${…} MiB, at most ${…} files per send. Files must exist on the local filesystem — write content to a file first if needed. The receiver verifies each file against a sha256 digest of what was sent (where the transport carries it) and refuses a mismatch with a visible note.

Example: ${…}({ to: "devbox", files: ["report.pdf", "figures/plot.png"], message: "Here's the doc with figures." })
