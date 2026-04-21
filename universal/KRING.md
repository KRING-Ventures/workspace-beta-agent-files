# KRING

Universal. Org context so the agent can speak KRING to its user. KRING the entity only — no individuals. People belong in the user's `USER.md`.

---

## What KRING is

**KRING Ventures** — a Danish venture studio and fund. KRING builds AI-native businesses: product flows, venture-building capability, and operational infrastructure. Not a consultancy. Not a pure fund. We build, incubate, and run.

## What KRING does

- **Spins up ventures** inside the KRING ecosystem — each with one product, one customer, one problem.
- **Runs a shared operating model** (Speedbooting OS — see `SPEEDBOOTING.md`) across every venture so the framework, not any single founder's memory, carries continuity.
- **Ships shared infrastructure**: personal AI agents (OpenClaw-powered), Notion, Slack, Google Workspace, GitHub, Obsidian, the Cosmica platform.
- **Invests in a learning year** — 2026 is explicitly a year of skill-building, framework-building, and cashflow. Treat this seriously in any work.

Current direction: AI-native business solutions; 2-year vision is "AI-driven businesses for a better world." Immediate priority: Learning & Cashflow.

## Current ventures (2026-04-21 snapshot)

- **Cosmica** — KRING's internal Speedbooting Platform. Canonical home for Speedblocks, Services, Idea Canvas. Notion → Cosmica sync feeds the Activity model (Strategic Initiatives + Management Priorities). Hosted on Render; code at `KRING-Ventures/Cosmica` on GitHub.
- **Carelog ApS** — AI clinical note-taking for Danish healthcare practitioners (psychologists, physicians, physios, psychiatrists, business psychologists). Record → transcribe → generate structured clinical note. CVR 45350916, founded 2026-01-20. Pricing: 349 DKK/mo Standard (solo), 299 DKK/mo per user Clinic (5+). D-Mærket certified. 14-day self-serve trial.

Active Speedblocks right now: **Workspace v1.0** (personal agents for the first 3 pilots, shipping 2026-04-22) and **Workspace v1.1** (MS → Google cutover, split from v1.0 on 2026-04-20).

## How KRING communicates

- **Slack** — primary ops comms. Threaded. Decisions log to Notion one-at-a-time as they land, not batched.
- **Notion** — source of truth for Speedblock state and Project Management. Canonical pages are never renamed.
- **Telegram** — personal OpenClaw agent surface.
- **Gmail / Google Workspace** — inbound notifications; important items surface into Slack or Notion. Basis stack for mail / calendar / files after v1.1.
- **Obsidian vault** — shared + personal knowledge. Project hierarchy: `projects/KRING/Speedbooting/Cosmica/{Speedblocks/Workspace/v1.x, Platform}`. Folder notes use same-name `.md` (never `README.md`). Breadcrumb parents, no orphans, strict tag taxonomy. Read vault governance before writing.
- **GitHub** — Cosmica + agent code. CodeRabbit reviews, Vercel preview deploys, Render production.

Language: Danish default, works in English. Tone: direct, specific, no filler. Direct communication is Danish norm, not rudeness.

## How KRING decides

- The Speedblock owner locks Scope and Solution. Building Briefs are the owner's alone to author — agents don't draft brief content.
- Platform architecture — migrations, infra cutovers, runtime changes — is locked by the platform owner.
- Decisions log to the Notion PM Tasks DB as they land. The PM task is the decision record.
- **"Locked"** = committed. **"Draft"** = proposal / WIP. Avoid retired framing (e.g. "Wave 1 / Wave 2").

## The Basis stack (Workspace 1.0 Solution)

Locked for the agent layer across the first 3 pilots: Google Workspace (incl. Gemini) · Slack · Notion · OpenClaw · Claude · GitHub · Obsidian (+ Syncthing). MS drops off the active stack; the MS → Google cutover runs in v1.1.

## What the agent should never assume about KRING

- Don't assume the stack matches any other startup. Default tools are listed above. Per-pilot OAuth scopes live in `TOOLS.md`.
- Don't infer Speedblock status from Slack chatter — read the Notion PM Tasks DB.
- Don't write to Obsidian without reading vault governance first.
- Don't conflate the org with any single person. This file is KRING the entity. The user's own relationship to KRING — their role, their people, their pain — lives in `USER.md`.

---

## For the agent reading this

- If a user asks a KRING question and the answer isn't in here, say so. Don't extrapolate.
- Framework detail (Speedbooting OS, lifecycle, deliverables) lives in `SPEEDBOOTING.md`. Coaching lens lives in `HUMAN_OS.md`. Canonical long-form references live in the Notion Master Brief and the `speedblock-master-brief` skill.
- This file is universal and grows. If you learn something stable about KRING, propose an update — don't edit silently.
