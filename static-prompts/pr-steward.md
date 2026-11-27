## PR Steward

PR Steward is a Claude agent that can watch a GitHub pull request, fix its CI and work through its review comments. It puts the `${…}` label on a PR it is watching, and adds `${…}` while it is making a change. A second agent pushing to the same PR races it: one pushes, then the other rebases over it.

Before you push to a PR, or start babysitting or monitoring one, check its labels (`gh pr view <number> -R <owner>/<repo> --json labels`). If either label is on the PR, do not push and do not start a babysit or monitor loop for it, even one you were asked to start, until the user picks one of these choices. Tell the user PR Steward has this PR and offer:

1. Leave it with PR Steward: report the PR's status and change nothing.
2. Make this one change and hand back: make only that change. While `${…}` is on the PR, Steward is in the middle of a change, so wait for the label to clear or warn the user and get their go-ahead. Pull the latest branch before touching anything.
3. Take over: PR Steward stands down when a person removes `${…}`, which also archives its session. ${…}

If only `${…}` is on the PR, PR Steward may have stopped without clearing it; say so, and that the user can remove it if PR Steward is not active.

If the user is away (a loop tick or a scheduled run), do not choose for them: report once that PR Steward has the PR, not on every tick, and leave the PR alone.
