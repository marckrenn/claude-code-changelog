# Tool Description: cron-create

- Name: CronCreate
- Source: native-prompt-markdown-tool

## Summary

Schedule a prompt for future execution.

# Raw Prompt Text
Schedule a prompt to be enqueued at a future time. Use for both recurring schedules and one-shot reminders.

Uses standard ${NUM}-field cron in the user's local timezone: minute hour day-of-month month day-of-week. "${NUM} ${NUM} * * *" means 9am local — no timezone conversion needed.

#### One-shot tasks (recurring: false)

For "remind me at X" or "at <time>, do Y" requests — fire once then auto-delete.
Pin minute${PATH} to specific values:
  "remind me at ${NUM}:30pm today to check the deploy" → cron: "${NUM} ${NUM} <today_dom> <today_month> *", recurring: false
  "tomorrow morning, run the smoke test" → cron: "${NUM} ${NUM} <tomorrow_dom> <tomorrow_month> *", recurring: false

#### Recurring jobs (recurring: true, the default)

For "every N minutes" / "every hour" / "weekdays at 9am" requests:
  "*/${NUM} * * * *" (every ${NUM} min), "${NUM} * * * *" (hourly), "${NUM} ${NUM} * * ${NUM}-${NUM}" (weekdays at 9am local)

#### Avoid the :${NUM} and :${NUM} minute marks when the task allows it

Every user who asks for "9am" gets `${NUM} ${NUM}`, and every user who asks for "hourly" gets `${NUM} *` — which means requests from across the planet land on the API at the same instant. When the user's request is approximate, pick a minute that is NOT ${NUM} or ${NUM}:
  "every morning around ${NUM}" → "${NUM} ${NUM} * * *" or "${NUM} ${NUM} * * *" (not "${NUM} ${NUM} * * *")
  "hourly" → "${NUM} * * * *" (not "${NUM} * * * *")
  "in an hour or so, remind me to..." → pick whatever minute you land on, don't round

Only use minute ${NUM} or ${NUM} when the user names that exact time and clearly means it ("at ${NUM}:${NUM} sharp", "at half past", coordinating with a meeting). When in doubt, nudge a few minutes early or late — the user will not notice, and the fleet will.

#### Durability

By default (durable: false) the job lives only in this Claude session — nothing is written to disk, and the job is gone when Claude exits. Pass durable: true to write to .claude${PATH} so the job survives restarts. If Claude Code can't tell which organization this session is signed in to, the job stays session-only even with durable: true. If the result says "Session-only" after durable: true, tell the user that the job won't survive restarts. Only use durable: true when the user explicitly asks for the task to persist ("keep doing this every day", "set this up permanently"). Most "remind me in ${NUM} minutes" / "check back in an hour" requests should stay session-only.

#### Not for live watching

CronCreate re-runs a prompt at fixed wall-clock intervals. To watch a log file, process, or command output and be notified the moment something changes, use the Monitor tool instead — Monitor streams events as they happen; cron polls on a schedule.

#### Runtime behavior

Jobs only fire while the REPL is idle (not mid-query). Durable jobs that were saved to .claude${PATH} survive session restarts — on the next launch signed in to the same organization they resume automatically. One-shot durable tasks that were missed while the REPL was closed are surfaced for catch-up. Session-only jobs die with the process. The scheduler shifts each job by a fixed per-job offset on top of whatever you pick: by default a recurring job runs up to ${NUM}% of its period late (max ${NUM} min), and a one-shot job landing on :${NUM} or :${NUM} runs up to ${NUM} s early. The result of this tool and of CronList gives each job's actual next run time: when you tell the user when a job will run, give that time, not the minute in the cron expression. Picking an off-minute is still the bigger lever.

Recurring tasks auto-expire after ${NUM} days — they fire one final time, with a note that it is their last run, then are deleted. This bounds session lifetime. Tell the user about the ${NUM}-day limit when scheduling recurring jobs.

Returns a job ID you can pass to CronDelete.
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "cron": {
      "description": "Standard ${NUM}-field cron expression in local time: \"M H DoM Mon DoW\" (e.g. \"*/${NUM} * * * *\" = every ${NUM} minutes, \"${NUM} ${NUM} ${NUM} ${NUM} *\" = Feb ${NUM} at ${NUM}:30pm local once).",
      "type": "string"
    },
    "prompt": {
      "description": "The prompt to enqueue at each fire time.",
      "type": "string"
    },
    "recurring": {
      "description": "true (default) = fire on every cron match until deleted or auto-expired after ${NUM} days. false = fire once at the next match, then auto-delete. Use false for \"remind me at X\" one-shot requests with pinned minute${PATH}",
      "type": "boolean"
    },
    "durable": {
      "description": "true = persist to .claude${PATH} and survive restarts (the result says Session-only if the job could not be saved). false (default) = in-memory only, dies when this Claude session ends. Use true only when the user asks the task to survive across sessions.",
      "type": "boolean"
    }
  },
  "required": [
    "cron",
    "prompt"
  ],
  "additionalProperties": false
}
