# KRING

Universal. Org context so the agent can speak KRING to its user. KRING the entity only — people belong in the user's `USER.md`.

---

## What KRING is

**KRING Ventures** — a Danish hybrid venture studio and fund. KRING partners with founders to build and invest in ventures that matter. Not a consultancy. Not a pure fund. KRING builds, incubates, invests, and operates inside each venture.

Official framing (kring.com): *"We partner with founders to build and invest in ventures that matter."*

## Why KRING exists

To build AI-native businesses that actually improve lives — with focus areas in **health, wellbeing, and sustainable energy**. Pre-seed and idea-stage. Deep involvement from day zero, not arm's-length capital.

## How KRING works — the hybrid model

The studio and the fund are one operation. Every venture goes through the studio before any fund commitment. Validation is fact- and signal-based; no vanity metrics. Ventures are either killed fast or scaled fast — there is no slow drift.

Five standing principles:

1. **All ventures go through the studio.** No exceptions. Studio work is the validation layer, not a nice-to-have.
2. **Validate on facts, data, and real signals** — not vanity or founder enthusiasm.
3. **Kill faster.** A quick no is worth more than a slow maybe.
4. **One team, clear mandates.** Studio, fund, and venture operators work from the same table with explicit ownership.
5. **AI-native by default.** Every venture assumes AI as a first-class component of the product and the operating model.

## The POD sprint plan

Venture building runs on a **24-week POD sprint**, structured around bi-weekly stage gates. Two ventures can run in parallel (Venture 1 / Venture 2 offset). Each gate is a real kill-or-continue decision made on signal — not a ceremonial review.

Long-form detail lives in the Hybrid Venture Studio reference.

## Active ventures (2026-04-22 snapshot)

- **Cosmica** — KRING's internal Speedbooting Platform. The canonical home for Speedblocks, Playbooks, Use-cases, and Roadmaps. Hosted on Render; code at `KRING-Ventures/Cosmica` on GitHub. Notion → Cosmica sync feeds the Activity model (Strategic Initiatives + Management Priorities).
- **Carelog ApS** — AI clinical note-taking for Danish healthcare practitioners (psychologists, physicians, physios, psychiatrists, business psychologists). Record → transcribe → structured clinical note. CVR 45350916, founded 2026-01-20. Pricing: 349 DKK/mo Standard (solo), 299 DKK/mo per user Clinic (5+). D-Mærket certified. 14-day self-serve trial.
- Earlier POD cohort learnings — **Spectia, Orklys, Sequence, Iris** — inform the current operating model (see Hybrid Studio reference).

## Active Speedblocks (2026-04-22)

- **Workspace v1.0** — personal OpenClaw agents (OPs) for the first 3 pilots. Ships today.
- **Workspace v1.1** — MS → Google cutover. Live to Google; MS read-only; best-effort Google copy + cold PST snapshot. Target 2026-04-30.
- **Workspace v1.2** — Meeting structure (IDOART) + Personal Assistant capabilities + Focus-time patterns. Target 2026-05-07.

## The Basis stack (locked 2026-04-22 for the agent layer)

- **Google Workspace** — mail, calendar, Drive, Docs, Meet, Gemini for in-product summaries.
- **Slack** — primary ops comms. Threaded. Decisions log one-at-a-time as they land.
- **Notion** — source of truth for Speedblock state and Project Management (PM Tasks DB).
- **OpenClaw** — agent runtime. Two agent layers: **Cosmo** (shared KRING-org agent) and **OP** (personal per user).
- **Claude** — general-purpose LLM reasoning.
- **GitHub** — code + agent file repos. CodeRabbit reviews, Vercel preview deploys, Render production.
- **Telegram** — OP surface (how each pilot talks to their personal agent).

MS drops off the active stack. v1.1 runs the cutover.

## The four AI layers

1. **Gemini** — inside Google Workspace. Doc-level and inbox-level summarisation.
2. **Claude** — general-purpose reasoning. Used by Cosmo and OP under the hood.
3. **OP** — each user's personal agent. Telegram-first. Personal name per pilot. Memory is private to that user.
4. **Cosmo** — the shared KRING-org agent. One instance. Lives in the OpenClaw workspace.

An OP is not a Cosmo clone. OP is personal and private; Cosmo is shared and org-wide. They coexist and hand off explicitly — never silently.

## How KRING communicates

- **Slack** — primary ops comms. Threaded. Decisions log to Notion as they land, not batched.
- **Notion** — source of truth for Speedblock state and PM Tasks DB. Canonical pages are never renamed; scope splits become the next sequential version (v1.0 → v1.1).
- **Telegram** — personal OP surface.
- **Gmail / Google Workspace** — inbound notifications; important items surface into Slack or Notion. Basis stack for mail / calendar / files after v1.1.
- **GitHub** — Cosmica + agent code. CodeRabbit reviews, Vercel preview deploys, Render production.

Language: Danish default, works in English. Tone: direct, specific, no filler. Direct communication is Danish norm, not rudeness.

## How KRING decides

- The **Speedblock owner** locks Scope and Solution. Owners author the Playbook, Use-cases, and Roadmap. Agents don't draft that content — agents assist, surface tension, log decisions.
- **Platform architecture** (migrations, infra cutovers, runtime changes) is locked by the platform owner.
- Decisions log to the Notion PM Tasks DB **as they land**, one at a time. The PM task is the decision record.
- **"Locked"** = committed. **"Draft"** = proposal / WIP. Avoid retired framing (e.g. "Wave 1 / Wave 2", "Building Brief").

## What the agent should never assume about KRING

- Don't assume the stack matches any other startup. Default tools are the Basis stack above. Per-pilot OAuth scopes live in `TOOLS.md`.
- Don't infer Speedblock status from Slack chatter — read the Notion PM Tasks DB.
- Don't conflate the org with any single person. This file is KRING the entity. The user's own relationship to KRING — their role, their people, their pain — lives in `USER.md`.
- Don't treat Cosmo context as OP context, or vice versa. Separate memories; separate surfaces.

---

## For the agent reading this

- If a user asks a KRING question and the answer isn't in here, say so. Don't extrapolate.
- Framework detail (Speedbooting OS, lifecycle, deliverable rules) lives in `SPEEDBOOTING.md`. Coaching lens lives in `HUMAN_OS.md`.
- This file is universal and grows. If you learn something stable about KRING, propose an update — don't edit silently.
