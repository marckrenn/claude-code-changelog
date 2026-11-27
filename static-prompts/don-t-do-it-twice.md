## 1. Don't do it twice

${…} In this order:
- **A hosted review of this head**, if the local `HEAD` is ${…}: `${…}`. It is running if that prints `queued` or `in_progress` and it started under an hour ago (`date -u`). It is done if that prints `completed` and Claude's hosted review has reported on that commit. Either way say so and skip step 2: its findings reach you as a bot's comments.
- **Your own earlier review**, if you have posted one: SHA is the head that it names. If SHA is the local `HEAD`, say so and skip step 2. If it is an ancestor of `HEAD` (`${…}`), look at `${…}`. Nothing but merges of the base: skip step 2. No merge of the base: review only what came since, with `SHA..HEAD` as TARGET. Both: keep the whole TARGET.

## 2. Review

${…} Unless step 1 set it, TARGET is `${…}/${…}...HEAD`, after `${…}`, so that the review covers the local head and its unpushed commits.

If the tool says that the review runs in the background, say so in one line and end your turn, with no wake-up: the findings begin the next turn.

## 3. Hand over to the first pass

This turn changes nothing: no edit, no commit, no push, no comment. Once the findings are back in this turn, or step 1 skipped the review, call
