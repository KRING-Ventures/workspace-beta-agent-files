# Workspace 1.0 — OpenClaw Agent File Set

Canonical files each pilot's personal OpenClaw agent ("OP") ships with. Authored 2026-04-22.

**Ship date:** 2026-04-22 (Workspace Speedblock v1.0)
**Pilots:** August Kring, Jesper Kring, Johan Rishede Duus
**Basis stack:** Google Workspace (incl. Gemini) · Slack · Notion · OpenClaw · Claude · GitHub · Telegram (OP surface)

## What this repo is

The **shared** file set for every OP. Universal files ship identically across all three pilots. Per-agent files are personalised from the template in `per-agent-template/` during BOOTSTRAP.

This is not the agent runtime. The runtime is OpenClaw; this is the file layer OpenClaw reads.

## Layout

```
universal/                       # ships identically with every OP
├── SOUL.md                      # character, boundaries, voice
├── AGENTS.md                    # session boot, memory, permissions
├── BOOTSTRAP.md                 # first-session onboarding dialogue
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

per-agent-template/              # blueprint copied into each pilot's folder
├── IDENTITY.md                  # name, role, vibe, emoji
├── USER.md                      # user profile (filled during BOOTSTRAP)
├── TOOLS.md                     # what's actually wired up
└── automations/
    └── AUTOMATIONS.md           # index of built automations

pilots/                          # per-pilot personalisation (stubs)
├── august/                      # August Kring's OP
├── jesper/                      # Jesper Kring's OP
└── johan/                       # Johan Rishede Duus's OP
```

## Two agent layers at KRING

- **Cosmo** — the shared KRING-org agent. One instance for the organisation. Runs in `/root/clawd/`. Not this repo.
- **OP** — each user's personal agent. Three instances in v1.0 (one per pilot). Built on this file set.

Gemini (in-product summaries inside Google Workspace) and Claude (general-purpose work) are the other two AI layers — they're tools OP and Cosmo use, not separate agents.

## Skills

Not in this repo. Skills live in the shared `openclaw-skills` GitHub repo. Each OP grants skills on demand; granted skills are recorded in that pilot's `TOOLS.md`. v1.0 ships the automation-builder skill as standard.

## Instantiation flow

1. Copy `universal/` and `per-agent-template/` into the new OP's workspace.
2. Run BOOTSTRAP.md as a dialogue with the user — fill `USER.md`, confirm `IDENTITY.md`, wire `TOOLS.md`.
3. Seed `MEMORY.md` and today's `memory/YYYY-MM-DD.md` with what came out of BOOTSTRAP.
4. Delete `BOOTSTRAP.md` from the live workspace. It's first-session only.

Placeholders (`{{AGENT_NAME}}`, `{{USER_FIRST_NAME}}`, etc.) use double curly braces. `{{FROM_BOOTSTRAP}}` markers are filled in-session, not during instantiation.

## Authoring state (2026-04-22)

- **Universal files** — authored against today's locked decisions. KRING.md sourced from kring.com/about + the Hybrid Venture Studio principles + in-flight project context. SPEEDBOOTING.md reflects the **Playbook + Use-cases + Roadmap** model locked 2026-04-22.
- **Per-agent template** — blueprint ready for personalisation.
- **Pilots** — stubs only. Each pilot's IDENTITY/USER/TOOLS is filled in BOOTSTRAP.

## Licence

MIT. See `LICENSE` in the repo root if/when added.
