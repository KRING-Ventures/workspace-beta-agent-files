# Workspace 1.0 — OpenClaw Agent File Set (shared layer)

The **shared framework layer** for every KRING OP (personal OpenClaw agent). Authored 2026-04-22.

**Ship date:** 2026-04-22 (Workspace Speedblock v1.0)
**Pilots:** August Kring, Jesper Kring, Johan Rishede Duus
**Basis stack:** Google Workspace (incl. Gemini) · Slack · Notion · OpenClaw · Claude · GitHub · Telegram (OP surface)

## What this repo is

The **shared** file set that ships identically with every OP — framework content (KRING context, Speedbooting rules, SOUL, AGENTS, BOOTSTRAP, HEARTBEAT, HUMAN_OS, memory templates, working templates) plus the `per-agent-template/` blueprint used when a new OP is instantiated.

**Personal context does not live here.** Each pilot's personal layer lives in their own private repo (see below). The OpenClaw runtime assembles both layers — shared + personal — at session boot.

This is not the agent runtime. The runtime is OpenClaw; this is the file layer OpenClaw reads.

## Layout

```
universal/                       # ships identically with every OP
├── SOUL.md                      # character, boundaries, voice
├── AGENTS.md                    # session boot, memory, permissions
├── BOOTSTRAP.md                 # first-session onboarding dialogue (run by the live OP)
├── HEARTBEAT.md                 # proactive check-in protocol
├── HUMAN_OS.md                  # 8-dimension coaching lens
├── KRING.md                     # KRING org context (the entity)
├── SPEEDBOOTING.md              # KRING delivery framework (Playbook + Use-cases + Roadmap)
├── MEMORY.md                    # long-term memory template
├── memory/
│   └── 2026-04-22.md            # example daily log
└── templates/
    ├── daily.md                 # morning brief
    ├── weekly.md                # Friday EOD brief
    └── email-draft.md           # email drafting structure

per-agent-template/              # blueprint cloned into each pilot's private repo
├── IDENTITY.md                  # name, role, vibe, emoji
├── USER.md                      # user profile (filled during BOOTSTRAP — by the OP itself)
├── TOOLS.md                     # what's actually wired up
└── automations/
    └── AUTOMATIONS.md           # index of built automations
```

## Private per-pilot repos

Each pilot's **personal layer** — `IDENTITY.md`, `USER.md`, `TOOLS.md`, `automations/`, their own `MEMORY.md` + `memory/` — lives in an independent private repo under `KRING-Ventures/`:

- `op-august` — August Kring's OP
- `op-jesper` — Jesper Kring's OP
- `op-johan` — Johan Rishede Duus's OP

These repos are private by design. Personal context never sits alongside shared framework content.

## Two agent layers at KRING

- **Cosmo** — the shared KRING-org agent. One instance for the organisation. Runs in `/root/clawd/`. Not this repo.
- **OP** — each user's personal agent. Three instances in v1.0 (one per pilot). Built on this framework + the pilot's private repo.

Gemini (in-product summaries inside Google Workspace) and Claude (general-purpose work) are the other two AI layers — they're tools OP and Cosmo use, not separate agents.

## Skills

Not in this repo. Skills live in the shared `openclaw-skills` GitHub repo. Each OP grants skills on demand; granted skills are recorded in that pilot's private `TOOLS.md`. v1.0 ships the **automation-builder** skill as standard.

## Instantiation flow (per OP)

At OpenClaw runtime, both layers are assembled:

1. Clone this repo (shared) — universal files + per-agent-template.
2. Clone the pilot's private `op-<pilot>` repo — personal files (already seeded with `{{FROM_BOOTSTRAP}}` markers).
3. **First live session:** the OP runs `universal/BOOTSTRAP.md` as a dialogue with its user. The OP fills its own `USER.md`, confirms its `IDENTITY.md` (agent name / vibe / emoji), and wires `TOOLS.md`. Seeds `MEMORY.md` and today's `memory/YYYY-MM-DD.md`.
4. `BOOTSTRAP.md` is deleted from the live workspace after session one. The canonical copy stays here in the shared repo.

Placeholders (`{{AGENT_NAME}}`, `{{USER_FIRST_NAME}}`, etc.) use double curly braces. `{{FROM_BOOTSTRAP}}` markers are filled **by the OP, during its own first session** — never by a central operator.

## Authoring state (2026-04-22)

- Universal files authored against today's locked decisions.
- KRING.md sourced from kring.com/about + the Hybrid Venture Studio principles + in-flight project context.
- SPEEDBOOTING.md reflects the **Playbook + Use-cases + Roadmap** model locked 2026-04-22.
- Per-agent template is blueprint-ready; BOOTSTRAP runs in each OP's live first session.

## Licence

MIT. See `LICENSE` in the repo root if/when added.
