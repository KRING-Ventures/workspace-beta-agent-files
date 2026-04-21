# Memory

Long-term memory for the agent. Structured, append-mostly. Daily activity lives in `memory/YYYY-MM-DD.md`; what gets promoted to this file is what the agent wants to remember across sessions indefinitely.

---

## User facts

Things about the user that are stable-ish and the agent uses regularly. Duplicates USER.md for fast access during generation; USER.md stays the source of truth — update both when facts change.

- (empty — seeded by BOOTSTRAP)

## Commitments (open)

Things the user said they'd do, waiting to land. With to-whom, by-when.

- (empty)

## Commitments (closed)

Recent closed commitments — kept for ~90 days to help the agent flag patterns.

- (empty)

## Decisions made

Decisions the user made and the agent should remember (so it doesn't re-raise). Include the context briefly.

- (empty)

## User preferences

Settled preferences — things the user has told the agent to always/never do. Cleaner than re-reading every memory log.

- (empty)

## Patterns observed

Agent-noted patterns worth carrying forward.

- (empty)

## Corrections

Times the user has told the agent "stop doing X" or "don't get this wrong again." Agent reads this before any risky action.

- (empty)

## Key events

Landmark events in the user's work/life the agent should know about (hire dates, major launches, team changes, personal things if shared).

- (empty)

---

## Update rules

- **Append, don't rewrite** — history matters. If a fact changes, mark the old one as superseded, add the new one dated.
- **Promote from daily logs** — at end of each week, review memory/YYYY-MM-DD.md for anything worth moving here.
- **Prune expired** — commitments that closed >90 days ago, patterns no longer relevant, preferences the user has since overridden.
- **Never silently edit** — if the user asks "why did you do X," the agent should be able to point to the memory entry that informed it.
- **Privacy** — memory is scoped to this user's agent only. Never share memory content across agents.
