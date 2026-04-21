# SPEEDBOOTING

Universal. The KRING delivery framework — what a Speedblock is, how it moves, what it produces, and the standing rules every agent must follow when working inside one.

Canonical long-form detail lives in the Notion Master Brief and the `speedblock-master-brief` skill references (`lifecycle.md`, `deliverables.md`, `operating-manual.md`, `construction-brief.md`, `quality-gates.md`, `prototype-rules.md`, `release-metadata.md`, `delivery-format.md`). This file is the operating summary.

---

## Core mantra

> *Think big, start small, scale fast.*

Every Speedblock starts with the full vision, then scopes ruthlessly to the smallest deliverable unit, then builds momentum through rapid iteration — at every level (Speedblock, stage, task).

## Two layers, kept separate

1. **Framework layer** — what a Speedblock *is* and how the system works. Lives in the Master Brief and the `speedblock-master-brief` skill references.
2. **Speedblock layer** — the packaged deliverables of a finished Speedblock.

Construction does not live in a separate document layer. It lives inside the Notion task hierarchy for that specific Speedblock. Don't blur these.

## Lifecycle

Three phases: **Build → Test → Publish.**

Build is where most agent work lives. Inside Build, stages run through **Scope → Research → Solution → Prototype → Learning → Blueprint**. Prototype is a fixed Build stage, not an optional shortcut — the solution must be proven in reality before formal packaging. Learning defines how the proven solution will be measured and kept healthy. Blueprint converts validated solution + learning logic into the full Speedblock package.

## Five core deliverables (the packaged output of a finished Speedblock)

1. **Value Brief** — why it exists, who it's for, what it's worth.
2. **Playbook** — how to run it.
3. **Toolkit** — what you need to run it.
4. **Onboarding** — deployment and adoption guide (formerly "Rollout Plan").
5. **Cosmo KF** — the Cosmo Knowledge File that lets the org agent run it forward.

## Task hierarchy in Notion PM

- Create the Speedblock as a **project in Project Overview** first. Fill project metadata (Status, Owner, Start Date, Finish Date, Blocked By, Category = Speedblock, Goal, About) before creating tasks.
- Task hierarchy: **head task → subphase → individual task.** The three head tasks are Build, Test, Publish.
- Under each subphase, keep **one subphase task** first. Standard stage elements live on that task's page as the initial content structure.
- **For Scope:** the main Scope task defines the overall problem space, affected users, boundaries, why-now, what's needed to move forward, and what counts as done. Create concrete Scope subtasks for real scoping jobs — not template headings. Name them after the real work. Don't add another task layer below this.
- **Every task page, at every level, gets operational text from the start:** clear goal, clear description, clear rule for what's needed to move to the next status, clear definition of done. A title alone is never enough.

## Versioning

- Speedblocks ship as v1.0, v1.1, etc. **Never rename a page** — scope splits or shifts become the next sequential version.
- Current state is read from **live project mapping statuses**, not canonical order alone. A later phase becomes next only when the current is Done.

## Standing rules (hard)

- **The Speedblock owner writes every Building Brief.** Agents don't draft or edit brief content.
- **Scope-stage Pain / Outcome / Impact must not name specific tools or delivery formats** — those belong in Research / Solution.
- **When Solution is locked, Solution is the source of truth** — not Research.
- **Already-embedded ≠ kept.** A tool/decision is only "kept" with an explicit decision. Otherwise it's open.
- **Success measures describe user value**, not agent activity.
- **Examples in briefs are illustrative, not prescriptive.**
- **Keep Status live** in the PM Tasks DB as work moves — not batched at the end.
- **Work inside the original stage task.** Spin-offs only when something fundamentally new surfaces, not for admin sub-steps.
- **Deadlines move honestly.** When a date slips, log the reason explicitly instead of drifting silently.
- **Never touch the Speedblock owner's Notion pages** (edits, inserts, reverts, cleanup) without explicit per-action permission.

---

## For the agent reading this

- When a user is working inside a Speedblock, this file is the reference. Don't improvise the framework.
- If a Speedblock decision conflicts with these rules, flag it — don't silently comply.
- Long-form detail and edge cases live in the skill references. Fetch them when this summary isn't enough.
