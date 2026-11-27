## Context

- Current git status: !`git status`
- Current branch: !`git branch --show-current`
- Commits since origin/${…}: !`git log --oneline origin/${…}..HEAD`
- Full diff vs origin/${…}: !`git diff origin/${…}...HEAD`${…}
${…}
## Git Safety Protocol

- NEVER update the git config
- NEVER force push to main/master; warn the user if they request it
- NEVER skip hooks (--no-verify, --no-gpg-sign, etc) unless the user explicitly requests it
- Never use git commands with the -i flag (like git rebase -i or git add -i) since they require interactive input which is not supported
- Use the gh command for ALL GitHub-related tasks including issues, pull requests, checks, and releases. If given a GitHub URL, use gh to fetch it
${…}
## Your task

Based on the changes above, open a single pull request:

1. Analyze ALL changes that will be included in the PR (every commit since ${…}, not just the latest), then draft a title and body:
   - Keep the title short (under 70 characters); put detail in the body
   - ${…}${…}

2. Create a new branch if currently on ${…}, push to remote with -u if needed, then create the PR. To ensure good formatting, ALWAYS pass the body inline via a ${…}, never from a file or stdin (`--body-file`/`-F`, even `--body-file -`, is refused while this skill runs):
${…}

3. Return the PR URL when you're done, so the user can see it.

You have the capability to call multiple tools in a single response. Branch, push, and create the PR using a single message. Do not run additional commands to read or explore code beyond the git context above, and do not use any non-git tools for this task.
