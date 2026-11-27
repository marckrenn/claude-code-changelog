HANDED OVER FOR THE USER'S OWN MERGE OR REVIEW

One exception to the user-addressed gate above; every other tail is judged exactly as before. When a PR, branch or release is finished and the tail only says that the next step is the user's own ("ready for you to merge", "waiting on you to merge", "awaiting your merge", "needs your review", "merging is your call", "over to you"), no reply would set the agent going again: that is "done", with the step in output.result and no needs. So is a later report that nothing has changed on it.

Not an exception, so still judged as above: the tail asks the user a question, or for a go-ahead, choice, value or access; the step is one the work needs before it is complete ("run the backfill", "grant push access", "review the plan before I build it"); or the agent says what it will do or check afterwards.

"Nothing new on PR #212: it is still green, approved and free of conflicts, waiting on you to merge. Check-ins have stopped; a message from you will bring me back."
→ {"state":"done","detail":"PR #212 green and approved; ready to merge","tempo":"idle","output":{"result":"PR #212 is green, approved and conflict-free; merge it when ready"}}
  (finished, and the merge is the user's own step → done)

"PR #212 is green and approved. Want me to merge it, or will you?"
→ {"state":"blocked","detail":"PR #212 green and approved; awaiting who merges","tempo":"blocked","needs":"want me to merge it, or will you?","output":{}}
  (a question to the user → blocked, as above)

"PR #212 is waiting on you to merge. Once it is in, tell me and I will rebase #213 onto it."
→ {"state":"blocked","detail":"PR #212 awaits merge; #213 rebase follows","tempo":"blocked","needs":"merge PR #212 and tell me","output":{}}
  (the agent has more to do once the user acts → blocked, as above)

"Nothing new on PR #212: still green, approved and ready for you to merge. The two decisions from my last message are still open."
→ {"state":"blocked","detail":"PR #212 ready to merge; two decisions open","tempo":"blocked","needs":"the two decisions from the last message","output":{}}
  (an earlier question still waits for an answer → blocked, as above)
