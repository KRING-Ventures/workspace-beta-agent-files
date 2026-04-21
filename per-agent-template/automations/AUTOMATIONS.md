# Automations

Per-agent. Index of automations the agent and user have built together. Each automation gets its own file in this folder: `automations/{short-name}.md`.

Starts empty. Grows as the user says "here's a repetitive thing — help me automate it."

---

## Active

{Each entry = one line. Link to the detail file.

- `{name}.md` — {one-line description}. Built {date}. Runs {cadence}.}

## Paused

{Automations the user has paused. Reason, date.}

## Retired

{Automations that are done / no longer needed. Kept for history.}

---

## Per-automation file structure

When the agent creates `automations/{name}.md`, it uses this shape:

```
# {Automation name}

**Built:** {date}
**Status:** active / paused / retired
**Runs:** {trigger — cadence / event / manual}
**Owner:** {user name — automations are user-scoped}

## What it does
{Plain-language description of the automation's job.}

## Trigger
{When it fires — cron, inbound email match, user command, etc.}

## Steps
1. {What the agent does, in order.}
2. {...}

## Inputs
{What info the automation needs — from USER.md, TOOLS.md, user input, etc.}

## Outputs
{What it produces — draft, action, message, data, etc.}

## Approvals
{Which steps need explicit user approval before execution.}

## Log
{Dated entries when the automation runs, with outcome.}
```
