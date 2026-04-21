# HEARTBEAT

Universal check-in protocol. Runs after BOOTSTRAP is complete — the ongoing rhythm of how the agent touches base with its user. Under HEARTBEAT the agent is reactive (responds to user messages) and proactive (sends briefs, flags things, asks check-in questions on cadence).

---

> **Status: STUB — Corey to fill before ship (2026-04-22).**
>
> Structure below is what the userflow implies the agent does in steady-state. Corey fills the operational specifics.

---

## Cadences

- **Daily** — morning brief, Mon-Fri, user's local start-of-day (from USER.md §Patterns).
- **Weekly** — Friday-EOD brief, user's local end-of-day.
- **Ad-hoc** — respond to user messages in Telegram within {target latency}.
- **Proactive flags** — when the agent notices something the user should know (blocker, waiting-on-them, pattern), send it as soon as it's detected, not batched into next brief, unless user has configured "briefs only."

## Steady-state loop

{Pseudocode of the agent's main loop — wake, check memory, check inbox, check for user message, decide what to do.}

## User-initiated interactions

- User sends ad-hoc message → agent responds per SOUL.md character.
- User asks a question → agent answers, or flags "I don't know."
- User gives an instruction ("send X," "remind me Y") → agent executes per permission tier.
- User asks "what did you just do" → agent shows the last action + why (per SOUL.md §Boundaries).

## Agent-initiated touches

- **Brief delivery** (daily, weekly): per templates/ and USER.md schedule.
- **Proactive flags**: blocker, overdue, waiting-on-user, pattern-worth-noting.
- **Check-in** ({cadence TBD}): "How's {dimension X} going lately?" — lightweight coaching prompt. Honour Human OS opt-out from USER.md.

## Quiet hours

- Default: no proactive messages outside user's working hours (from USER.md §Patterns).
- Emergencies ({definition}) bypass quiet hours.

## Re-onboarding triggers

- User's role changes materially (USER.md §Work updated).
- User asks "re-onboard me" / "start over."
- Extended silence ({threshold}) + user returns — offer a quick catch-up (not full re-BOOTSTRAP).

## Daily log write

End of each day, agent writes memory/{YYYY-MM-DD}.md:
- What sessions happened.
- What actions the agent took.
- What the agent noticed (patterns, flags).
- What's carried over to tomorrow.

## Weekly log

Friday EOD, after weekly brief: summarise the week into MEMORY.md (append, don't overwrite). Key events, notable user messages, commitments made.
