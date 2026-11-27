A SESSION THAT TALKS TO PEOPLE IN A CHAT THREAD

This agent works for people in a chat thread and reaches them only through the messages it posts there. The tail holds this turn in the order it happened, the agent's own notes and the messages it posted side by side; the posts are what the people read. It names people instead of saying "you". Where the rules above differ, these win:

  • A named person the agent is answering or working for IS the user. "Awaits Priya's go", "waiting on Priya's reply", "Priya to pick A or B", "needs Priya's approval / review / merge / publish" are user-addressed gates, not third-party waits.
  • A gate like that, a labelled open question or decision, or a step only that person can do is "blocked" while it is open, with needs = that ask, wherever it sits in the tail and however much else the turn finished. It is closed only when the tail says the person answered, or the agent handled or dropped it.
  • A scheduled check-in beside an open gate ("Next check in 20m", "I'll look again in an hour") is a safety net, not the agent's next step: still "blocked". With no open gate, the re-poll rules above stand.
  • Current state "blocked" and a turn that reports nothing new and no answer from the person ("no reply yet", "no change since the last check") stays "blocked"; needs says what it still waits for.
  • Every other wait stays as above: other teams' reviewers, code owners, a stamp channel, CI, a merge queue, a deploy, a timer, nobody. An optional offer after a delivery is still "done".

"PR #212 is up, CI is green and the migration note is in the description. Awaits Priya's go to merge. Next check in 30m."
→ {"state":"blocked","detail":"PR #212 green; awaits Priya's go to merge","tempo":"blocked","needs":"Priya's go to merge PR #212","output":{}}
  (Priya is the user; the check-in is a safety net → blocked)

Current state blocked: "Check-in: no reply in the thread, nothing new on PR #212. Next check in 1h."
→ {"state":"blocked","detail":"no reply yet on merging PR #212","tempo":"blocked","needs":"go-ahead to merge PR #212","output":{}}
  (nothing new and no answer → the earlier ask still stands)

"Priya approved PR #212 and it is in the merge queue. Next check in 10m."
→ {"state":"working","detail":"PR #212 approved; in the merge queue","tempo":"idle","output":{}}
  (the person has acted; the wait is on the queue and the agent re-checks → working)

"Told Priya the flaky test is fixed in PR #212. It now waits on the storage team's code-owner review."
→ {"state":"done","detail":"flaky test fixed in PR #212; awaiting code-owner review","tempo":"idle","output":{"result":"flaky test fixed in PR #212"}}
  (the reviewers are a third party and the agent plans nothing more → done)
