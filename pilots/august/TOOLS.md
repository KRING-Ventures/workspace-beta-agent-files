# Tools

Per-agent. What is actually wired up and authorised for this user. Corey pre-fills the baseline at deploy; BOOTSTRAP §4 and ongoing sessions update as the user grants/revokes access.

---

## Surfaces

| Surface  | Status     | Notes                  |
|----------|------------|------------------------|
| Telegram | {wired}    | Primary user surface   |
| Web UI   | {n/a 1.0}  | Later version          |

## Integrations (OAuth / tokens)

| Integration        | Scopes granted            | Status       | Notes                  |
|--------------------|---------------------------|--------------|------------------------|
| Google Calendar    | {read / read+write / n/a} | {pending/granted/declined} |                  |
| Gmail              | {read / read+compose-draft / n/a} | {status} | Agent drafts, never sends directly |
| Notion             | {read / read+write / n/a} | {status}     | User's personal workspace       |
| GitHub             | {skills-repo read / n/a}  | {wired}      | For skill fetch — Corey-wired   |

## Granted skills (from GitHub skills repo)

| Skill name         | Version | Granted date | Notes |
|--------------------|---------|--------------|-------|
| {e.g., automation-builder} | {ver}   | {date}       | Offered during BOOTSTRAP §7 |

If no skills granted yet: "None yet — user hasn't requested any."

## Declined / revoked

{If the user declines an integration or revokes one, log here with a dated entry so the agent doesn't re-prompt.

- 2026-04-22 — {integration} declined. Reason (if given): {}.}

## Local resources

{Anything the agent has local access to — files, memory directory, template directory. Just the paths, for auditability.}

- `SOUL.md` · `AGENTS.md` · `BOOTSTRAP.md` · `HEARTBEAT.md` · `HUMAN_OS.md` · `KRING.md`
- `templates/daily.md` · `templates/weekly.md` · `templates/email-draft.md`
- `IDENTITY.md` · `USER.md` · `TOOLS.md` (this file)
- `MEMORY.md` · `memory/` (daily logs)
- `automations/AUTOMATIONS.md` + `automations/{name}.md`

---

## Update log

- 2026-04-22 — Initial deploy by Corey.
