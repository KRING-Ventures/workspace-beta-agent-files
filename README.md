# Workspace 1.0 — OpenClaw Agent File Set

The files each pilot's personal OpenClaw agent ships with. Authored 2026-04-21 against the locked file structure in the Workspace 1.0 Deliverables task.

Ship date: 2026-04-22. Pilots: August Kring, Jesper Kring, Juhan Rishede Duus.

## Structure

```
universal/                    # Ships identically with every agent
├── SOUL.md                   # character, boundaries, voice
├── AGENTS.md                 # session boot, memory arch, permission model (Corey to fill)
├── BOOTSTRAP.md              # first-session onboarding script
├── HEARTBEAT.md              # check-in protocol (Corey to fill)
├── HUMAN_OS.md               # 8-dimension coaching framework (August to fill)
├── KRING.md                  # org context (August to fill)
├── MEMORY.md                 # long-term memory template
├── memory/
│   └── 2026-04-22.md         # example daily log
└── templates/
    ├── daily.md              # daily morning brief template
    ├── weekly.md             # Friday-EOD weekly brief template
    └── email-draft.md        # email drafting structure

per-agent-template/           # Blueprint copied into each pilot's folder
├── IDENTITY.md               # name, role, who they work for, vibe, emoji
├── USER.md                   # user profile, filled during BOOTSTRAP
├── TOOLS.md                  # what's wired up for this user
└── automations/
    └── AUTOMATIONS.md        # index of built automations

pilots/
├── august/                   # August Kring's agent
├── jesper/                   # Jesper Kring's agent
└── juhan/                    # Juhan Rishede Duus's agent
```

## Authoring state (2026-04-21)

- **Cosmo-authored** (ready for review): SOUL.md, BOOTSTRAP.md, templates/*, MEMORY.md + memory example, per-agent-template scaffolds.
- **August-authored** (stubs with skeletons to fill): KRING.md, HUMAN_OS.md.
- **Corey-authored** (stubs): AGENTS.md, HEARTBEAT.md.
- **Per-pilot personalisation** (stubbed, to fill before deploy): IDENTITY.md, USER.md, TOOLS.md for each of August/Jesper/Juhan.

## Skills

Not in this repo. Live in the GitHub skills repo. Each agent grabs what it needs on demand; granted-skill scopes are recorded in that user's TOOLS.md.
