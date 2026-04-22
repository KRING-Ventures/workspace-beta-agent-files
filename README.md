# Workspace 1.0 — OpenClaw Agent File Set (shared layer)

The **shared framework layer** for every KRING personal OpenClaw agent. Authored 2026-04-22.

**Ship date:** 2026-04-22 (Workspace Speedblock v1.0)
**Pilots:** August Kring, Jesper Kring, Johan Rishede Duus
**Standard tool set (v1.0):** Google Workspace (Calendar / Email / Drive) · Telegram · Notion · GitHub · web search · local files

## What this repo is

The **shared** file set that ships identically with every personal OpenClaw agent — framework content (KRING context, SOUL, AGENTS, BOOTSTRAP, HEARTBEAT, HUMAN_OS, memory templates, working templates) plus the per-pilot blueprint files (IDENTITY, USER, TOOLS, automations/) used when a new agent is instantiated.

**Personal context does not live here.** Each pilot's personal layer lives in their own private repo (see below). The OpenClaw runtime assembles both layers — shared + personal — at session boot.

This is not the agent runtime. The runtime is OpenClaw; this is the file layer OpenClaw reads.

## Layout

One flat set of canonical templates. Files marked **(per-pilot)** are blueprints cloned into each pilot's private repo and personalised; everything else ships identically.

```
SOUL.md                # character, boundaries, voice
AGENTS.md              # session boot, memory, permissions
BOOTSTRAP.md           # first-session onboarding dialogue (run by the live OpenClaw agent)
HEARTBEAT.md           # proactive check-in protocol
HUMAN_OS.md            # 8-dimension coaching lens
KRING.md               # KRING org context (the entity)
MEMORY.md              # long-term memory template
IDENTITY.md            # name, role, vibe, emoji  (per-pilot)
USER.md                # user profile, filled during BOOTSTRAP  (per-pilot)
TOOLS.md               # what's actually wired up  (per-pilot)
memory/
└── 2026-04-22.md      # example daily log
templates/
├── daily.md           # morning brief
├── weekly.md          # Friday EOD brief
└── email-draft.md     # email drafting structure
automations/
└── AUTOMATIONS.md     # index of built automations  (per-pilot)
```

## Private per-pilot repos

Each pilot's **personal layer** — `IDENTITY.md`, `USER.md`, `TOOLS.md`, `automations/`, their own `MEMORY.md` + `memory/` — lives in an independent private repo under `KRING-Ventures/`:

- `op-august` — August Kring's personal OpenClaw agent
- `op-jesper` — Jesper Kring's personal OpenClaw agent
- `op-johan` — Johan Rishede Duus's personal OpenClaw agent

These repos are private by design. Personal context never sits alongside shared framework content.

## Two agent layers at KRING

- **Cosmo** — the shared KRING-org OpenClaw agent. One instance for the organisation. Runs in `/root/clawd/`. Not this repo.
- **Personal OpenClaw agent** — one per user. Three instances in v1.0 (one per pilot). Built on this framework + the pilot's private repo.

## Skills

Not in this repo. Skills live in the shared KRING claw repo at https://github.com/KRING-Ventures/claw-shared (private). Each agent loads skills on demand; non-default scopes are recorded in that pilot's private `TOOLS.md`.

## Instantiation flow (per agent)

At OpenClaw runtime, both layers are assembled:

1. Clone this repo (shared) — all framework + blueprint files.
2. Clone the pilot's private `op-<pilot>` repo — personal files (already seeded with `{{FROM_BOOTSTRAP}}` markers).
3. **First live session:** the OpenClaw agent runs `BOOTSTRAP.md` as a dialogue with its user. The agent fills its own `USER.md`, confirms its `IDENTITY.md` (agent name / vibe / emoji), and wires `TOOLS.md`. Seeds `MEMORY.md` and today's `memory/YYYY-MM-DD.md`.
4. `BOOTSTRAP.md` is deleted from the live workspace after session one. The canonical copy stays here in the shared repo.

Placeholders (`{{AGENT_NAME}}`, `{{USER_FIRST_NAME}}`, etc.) use double curly braces. `{{FROM_BOOTSTRAP}}` markers are filled **by the OpenClaw agent, during its own first session** — never by a central operator.

## Authoring state (2026-04-22)

- Framework files authored against today's locked decisions.
- KRING.md sourced from kring.com/about + the Hybrid Venture Studio principles + in-flight project context.
- Per-pilot blueprint files are template-ready; BOOTSTRAP runs in each agent's live first session.

## Licence

MIT. See `LICENSE` in the repo root if/when added.
