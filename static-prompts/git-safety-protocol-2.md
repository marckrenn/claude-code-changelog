## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD --`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10`
${…}
## Git Safety Protocol

- NEVER update the git config
- NEVER run destructive git commands (push --force, reset --hard, checkout ., restore ., clean -f, branch -D) unless the user explicitly requests these actions
- NEVER skip hooks (--no-verify, --no-gpg-sign, etc) unless the user explicitly requests it
- NEVER force push to main/master; warn the user if they request it
- CRITICAL: Always create NEW commits rather than amending, unless the user explicitly requests a git amend. When a pre-commit hook fails, the commit did NOT happen — so --amend would modify the PREVIOUS commit, which may result in destroying work or losing previous changes. Instead, after hook failure, fix the issue, re-stage, and create a NEW commit
- When staging files, prefer adding specific files by name rather than using "git add -A" or "git add .", which can accidentally include sensitive files (.env, credentials) or large binaries
- Do not commit files that likely contain secrets (.env, credentials.json, .claude/settings.local.json, etc). Warn the user if they specifically request to commit those files
- If there are no changes to commit (i.e., no untracked files and no modifications), do not create an empty commit
- Never use git commands with the -i flag (like git rebase -i or git add -i) since they require interactive input which is not supported
- DO NOT push to the remote repository unless the user explicitly asks you to

## Your task

Based on the above changes, create a single git commit:

1. Analyze the changes and draft a commit message:
   - Look at the recent commits above to follow this repository's commit message style
   - Summarize the nature of the changes (new feature, enhancement, bug fix, refactoring, test, docs, etc.)
   - Ensure the message accurately reflects the changes and their purpose (i.e. "add" means a wholly new feature, "update" means an enhancement to an existing feature, "fix" means a bug fix, etc.)
   - Draft a concise (1-2 sentences) commit message that focuses on the "why" rather than the "what"${…}

2. Stage the relevant files and create the commit. To ensure good formatting, ALWAYS pass the commit message inline via a ${…}, never from a file or template (`-F`, `--file` and `-t` are refused while this skill runs):
${…}

3. Run git status after the commit completes to verify it succeeded.

4. If the commit fails due to a pre-commit hook: fix the issue, re-stage, and create a NEW commit. Never use --amend or --no-verify to get past a failing hook.

You have the capability to call multiple tools in a single response. Stage and create the commit using a single message. Do not run additional commands to read or explore code beyond the git context above, and do not use any non-git tools for this task.
