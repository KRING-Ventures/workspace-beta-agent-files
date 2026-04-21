# AGENTS

Universal ops manual. Session boot sequence, memory architecture, permission model. This is Corey's domain — the operational layer under every personal agent.

---

> **Status: STUB — Corey to fill before ship (2026-04-22).**
>
> The sections below are the shape Cosmo expects from the userflow + file set. Corey fills with the actual implementation details.

---

## Session boot sequence

What happens the moment the agent wakes up for a session.

1. {Load IDENTITY.md — who am I, who do I work for}
2. {Load SOUL.md — character, boundaries, voice}
3. {Load USER.md — user profile}
4. {Load TOOLS.md — what's available}
5. {Load KRING.md + HUMAN_OS.md — context}
6. {Load templates/* as needed (lazy or eager — Corey's call)}
7. {Check MEMORY.md + recent memory/*.md for last session state}
8. {Determine: first-session (run BOOTSTRAP) or steady-state (run HEARTBEAT)}

## Memory architecture

- **Short-term** (within a session): {how session context is held}
- **Long-term** (persistent): MEMORY.md is the structured index. memory/YYYY-MM-DD.md are daily logs.
- **Write rules**: {when does the agent write to memory, how is it structured, what gets promoted from daily-log to MEMORY.md}
- **Read rules**: {how the agent searches memory when it needs context}
- **Retention**: {how long daily logs stick around, summarisation strategy}

## Permission model

Tiered by irreversibility:

- **Read-only** (brief-generation, lookups): {auto-allowed}
- **Local write** (memory, user files): {auto-allowed}
- **User-visible output** (drafts in Telegram): {auto-allowed}
- **External effect** (sending emails, creating meetings, committing, posting): {requires explicit user approval per action}
- **Destructive** (deleting user data, revoking access): {requires extra confirmation, and logged}

## Skill invocation

- Skills live in the GitHub skills repo.
- Agent consults TOOLS.md §Granted skills to know what this user has authorised.
- {How skills are fetched — on-demand pull? pre-cached? auth model?}
- {How skill output is surfaced to the user vs stored}

## Failure modes

- {Telegram unreachable}
- {Tool auth expired}
- {Model API failure}
- {Memory corruption}
- {Skill load failure}

## Logs

- What gets logged, where, for how long.
- What the user can see (always) vs what's internal.

## Update path

- How do changes to universal files (SOUL.md, KRING.md, HUMAN_OS.md, templates/*) propagate to running agents?
- Version pinning or live-sync?
