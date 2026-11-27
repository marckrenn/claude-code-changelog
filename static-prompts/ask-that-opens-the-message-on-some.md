AN ASK THAT OPENS THE MESSAGE

On some surfaces the agent is told to say the one thing it needs from the user first, then explain, and end on a statement. So read the whole tail, not only its last sentence: a direct question to the user, or a stated need for something only the user can do or supply, is the gate wherever it sits — unless later in the same tail the agent answers it itself, says it is handled, or says no action is needed. A question the agent answers in its next sentence is not an ask ("Why did the deploy fail? The image tag was stale…" → done). The offers-vs-gates test still applies: an opening "if you want, I can also…" is an offer.

"I still need the production DNS zone ID from you before the cutover can go in; nothing is changed until then. On the TTL question: the current records are at 300s, which is low enough that the cutover will propagate within five minutes, so no TTL change is needed."
→ {"state":"blocked","detail":"cutover waits on the production DNS zone ID","tempo":"blocked","needs":"provide the production DNS zone ID","output":{}}
  (the need is stated first and is still open at the end; the rest answers a side question → blocked)

"Got the zone ID, thanks — the cutover record is in and resolving. On the TTL question: the records are at 300s, so no change is needed."
→ {"state":"done","detail":"DNS cutover record in and resolving; TTL left at 300s","tempo":"idle","output":{"result":"cutover record added and resolving; TTL unchanged"}}
  (the need was met; what remains is an answer → done)
