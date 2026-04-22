# SPEEDBOOTING

Universal. The KRING delivery framework — what a Speedblock is, how it moves, what it produces, and the standing rules every agent must follow when working inside one.

---

## Core mantra

> *Think big, start small, scale fast.*

Every Speedblock starts with the full vision, then scopes ruthlessly to the smallest deliverable unit, then builds momentum through rapid iteration — at every level (Speedblock, stage, task).

## What a Speedblock is

A **Speedblock** is a self-contained, shippable unit of value. One product, one customer, one problem — packaged so another venture or operator can pick it up and run it. Speedblocks live in **Cosmica** (KRING's internal Speedbooting Platform).

Speedblocks are the unit of work inside every POD sprint. They're how ideas convert into live, operating business value.

## Lifecycle

Three phases: **Build → Test → Publish.**

- **Build** — scope, research, solution lock, prototype, validate.
- **Test** — run the solution in reality against real users. Prove it works, harden it, measure.
- **Publish** — package and ship the three deliverables (below) into Cosmica.

Build is where most agent work lives. Inside Build, stages run through **Scope → Research → Solution → Prototype → Learning**. Prototype is a fixed Build stage, not an optional shortcut — the solution must be proven in reality before publishing.

## The three deliverables (the packaged output of a finished Speedblock)

**Locked 2026-04-22.** These replace the previous Building Brief + five-deliverable model.

### 1. Playbook

The operating document. Four standing sections:

- **Prerequisite** — what must be true before you start. Conditions, inputs, access, readiness.
- **Procedure** — the actual steps. How the work runs, in order, with decisions and handoffs named.
- **Tech stack** — the tools that run the procedure. Only the tools actually used; nothing aspirational.
- **Onboarding** — how a new user (or agent) gets from zero to running the Playbook. Self-serve wherever possible.

The Playbook is the source of truth for how the Speedblock operates.

### 2. Use-cases

One or two concrete examples of the Playbook in action. Not hypothetical — actual runs, with real inputs, real outputs, and real learnings. Use-cases prove the Playbook works outside the author's head.

- Minimum: 1 use-case (the Playbook doesn't count as published without it).
- Typical: 2 use-cases — one canonical, one edge-adjacent.
- Each use-case names: who ran it, when, what happened, what would they do differently.

### 3. Roadmap / Timeline

Versioned forward view. Where this Speedblock is going — v1.0, v1.1, v1.2, etc. — with honest dates and explicit scope per version.

- Dates are commitments, not aspirations.
- When a date slips, log the reason explicitly. Don't drift silently.
- Never rename a version. v1.0 stays v1.0; scope shifts become the next number.

## The 6-slide internal presentation

Every published Speedblock ships with a **6-slide internal presentation** for KRING-internal communication. Always the same shape:

1. **Cover** — name, version, owner, ship date.
2. **Objective** — Pain / Outcome / Impact. Why this exists. Who it's for. What it's worth.
3. **Roadmap** — versions + timeline.
4. **Demo** — Cosmica / Speedblock walkthrough with onboarding path.
5. **How we approached it** — the honest path from scope to ship (what changed, what didn't).
6. **Learnings** — painfully honest. What surprised us. What we'd do differently. What the org should take away.

The presentation is a communication artefact, not a replacement for the Playbook. The Playbook is operational; the presentation is narrative.

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

- **The Speedblock owner authors Playbook, Use-cases, and Roadmap.** Agents don't draft that content. Agents assist, surface tension, log decisions.
- **Scope-stage Pain / Outcome / Impact must not name specific tools or delivery formats** — those belong in Research / Solution / the Playbook's Tech stack section.
- **Pain / Outcome / Impact bullets must be short headline phrases** — `**bold label — short tail**`, not full sentences.
- **When Solution is locked, Solution is the source of truth** — not Research.
- **Already-embedded ≠ kept.** A tool or decision is only "kept" with an explicit lock. Otherwise it's open.
- **Success measures describe user value**, not agent activity. "User gets X without doing Y" beats "agent did Z".
- **Examples in references and prior Speedblocks are illustrative, not prescriptive.** Apply the rules to the current work; don't copy example shapes as mandates.
- **Keep Status live** in the PM Tasks DB as work moves — not batched at the end.
- **Work inside the original stage task.** Spin-offs only when something fundamentally new surfaces, not for admin sub-steps.
- **Deadlines move honestly.** When a date slips, log the reason explicitly instead of drifting silently.
- **Never rename a Notion page.** Splits and shifts create the next sequential version.
- **Never touch the Speedblock owner's Notion pages** (edits, inserts, reverts, cleanup) without explicit per-action permission.

## What changed on 2026-04-22

- The previous **Building Brief** is retired. The Playbook + Use-cases + Roadmap triplet replaces it.
- The previous five-deliverable model (Value Brief / Playbook / Toolkit / Onboarding / Cosmo-KF) is retired. Prerequisite / Procedure / Tech stack / Onboarding now live as **sections inside the Playbook**, not separate documents.
- The 6-slide internal presentation is now standard for every published Speedblock.

---

## For the agent reading this

- When a user is working inside a Speedblock, this file is the reference. Don't improvise the framework.
- If a Speedblock decision conflicts with these rules, flag it — don't silently comply.
- Long-form detail (lifecycle mechanics, Scope operating manual, prototype rules, release metadata) lives on the Speedblock-framework pages in Notion and in the `speedblock-master-brief` skill references. Fetch them when this summary isn't enough.
