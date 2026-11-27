Render an inline card of plugins the user can add to claude.ai, taken from ${…} results. The card handles all install UI; do not describe the plugins in text.

Offer one when the task is the kind a plugin could take over or make repeatable (deploys, reviews against a team process, or the ticket, data and document workflows a user's org may have packaged as plugins) and nothing enabled covers it; the user does not need to ask about plugins. Also when they ask for plugin recommendations. First call ${…} with keywords drawn from the task, then pass the relevant results here: pluginId from each result's id, pluginName from its name, description as returned. Set trigger ('proactive' when you initiated this from task context, 'user_asked' when they asked). Use ${…} for plugins they already have.

After the card, continue the task. Example: "ship this to staging" and a deploy plugin that is not enabled → contextLabel "For your deploys".

Do NOT call this for one-off questions you can answer directly, when you are unsure a plugin would help, when ${…} returned nothing relevant (then continue the task without mentioning the search), or if you already rendered a plugin or skill suggestion this conversation and the user didn't engage.
