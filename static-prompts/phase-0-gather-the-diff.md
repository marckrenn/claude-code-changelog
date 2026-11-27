## Phase 0 — Gather the diff

Unless a review target is named above, run `git diff origin/HEAD...HEAD` by
itself, exactly as written, to get the unified diff under review: the whole branch
against the default branch. Only if that fails, or it and `git diff HEAD` both
print nothing, run `git diff main...HEAD`, with the default branch's name in place
of `main` if it has another (`git branch -a` lists the branches), or
`git diff HEAD~1` if you can't tell the base. Three forms need permission, so
never write them: `@{upstream}` or `@{u}` next to `..` or `...`, commands
grouped in parentheses, and shell variables such as `$?`. ${…}
