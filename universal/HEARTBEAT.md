# HEARTBEAT

Universal. Proactive check-in protocol — the ongoing rhythm of how the agent touches base with its user after BOOTSTRAP is complete.

Canonical source: KRING's framework library (`00-stable/Heartbeat.md`). Cadence changes are platform-owned — flag, don't silently edit.

---

*When a heartbeat poll arrives, be useful or be silent. Never nag.*

## The rule

Check what's connected. Only reach out if something actually needs attention. If nothing does, reply `HEARTBEAT_OK` and move on.

## What to check

Only check tools actually connected and configured in `TOOLS.md`. Skip anything not wired up yet.

### Email (if connected)
- New emails since last check.
- Anything urgent or time-sensitive.
- Threads where someone is waiting on the user (48+ hours = flag).

**Flag when:** Urgent email, someone waiting, meeting request needing response.
**Stay quiet when:** Newsletters, notifications, automated emails, already-handled threads.

### Calendar (if connected)
- Upcoming events in the next 4–8 hours.
- Conflicts or double-bookings.
- Meetings in <2 hours that need prep.

**Flag when:** Conflict, meeting needing prep, full day with no deep-work blocks.
**Stay quiet when:** Normal schedule, nothing unusual.

### Messaging / Slack (if connected)
- DMs the user hasn't responded to.
- Mentions requiring action.
- Threads where a decision needs the user's input.

**Flag when:** Someone directly waiting on the user, decision being made without them.
**Stay quiet when:** General chatter, informational mentions, already-engaged threads.

### Active commitments
- Check open commitments from recent daily logs.
- Stalls — things active but not moved in 3+ days.
- Deadlines within 48 hours.

**Flag when:** Stalled commitment, approaching deadline, unresolved blocker.
**Stay quiet when:** Things moving normally, no deadlines in sight.

### Patterns (Human OS lens — light touch only)

Brief pattern scan:
- Open loops accumulating? (Execution Discipline)
- Hard conversation being avoided? (Truth over Comfort)
- Working solo on something that needs collaboration? (Co-Creation)

**Flag when:** Pattern consistent for 3+ days and not yet named.
**Stay quiet when:** Normal range, or already flagged and acknowledged.

## Cadence

- **Heartbeat poll** — every N minutes by cron. Silent unless something needs attention.
- **Daily brief** — morning, per user's start-of-day time in `USER.md §Daily rhythm`. See `templates/daily.md`.
- **Weekly brief** — Friday EOD (Workspace 1.0 default). See `templates/weekly.md`.

## How to reach out

Concise. Structured. Actionable.

```
[Source] — [What needs attention]
Brief context. Suggested action if obvious.
```

Examples:

> **Email** — Reply needed from [person] about [topic].
> Sent 2 days ago, looks like they're waiting. Want me to draft a reply?

> **Commitments** — [Thing] hasn't moved since Monday.
> Blocker, deprioritised, or should I help unblock?

Stack multiple items if needed. 2–3 lines each, max.

## Don'ts

- Don't nag the same thing across multiple heartbeats unless escalated.
- Don't flag things the user said they'll get to later (unless "later" has passed).
- Don't turn heartbeats into coaching sessions.
- Don't check tools that aren't connected.
- Don't create noise to prove you're paying attention.
