# TOOLS — {{AGENT_NAME}}'s Tool Configuration

*Reference for tool-specific setup, access details, and usage notes. Don't store credentials in other files.*

## Connection status

Track what's actually wired up. Heartbeats and operations only check connected tools.

| Tool | Status | Notes |
|---|---|---|
| Gmail (Google Workspace) | ❌ Not connected | |
| Google Calendar | ❌ Not connected | |
| Google Drive / Docs | ❌ Not connected | |
| Slack | ❌ Not connected | |
| Notion | ❌ Not connected | |
| GitHub | ❌ Not connected | |
| Telegram (OP surface) | ❌ Not connected | Primary surface — wire first. |
| Claude (general reasoning) | ✅ Available | Via OpenClaw harness. |
| Gemini (in-product summaries) | ✅ Available in Google Workspace | Not a separate skill. |
| Workspace files | ✅ Local | `{{WORKSPACE_PATH}}` |
| Web search / fetch | ✅ Available | |

*Update this table as tools are connected. `HEARTBEAT.md` checks this to know what to scan.*

## Granted skills

v1.0 ships with the **automation-builder** skill as standard. Log additional skills granted here:

| Skill | Granted | Scope / notes |
|---|---|---|
| automation-builder | {{TODAY}} | Standard v1.0 skill. Scope: build and modify user-facing automations inside the Basis stack. |

---

## Gmail (Google Workspace)

- **Account:** [email address]
- **Access:** [OAuth scope / skill name]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Never send without permission (see `AGENTS.md`).
  - Draft replies in workspace before sending. Use `templates/email-draft.md`.
  - Match {{USER_FIRST_NAME}}'s tone to each recipient.

## Google Calendar

- **Account:** [linked to Gmail above]
- **Access:** [OAuth scope / skill name]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Read freely, modify only with permission.
  - Flag conflicts proactively during heartbeats.
  - Protect deep-work blocks.

## Google Drive / Docs

- **Account:** [linked]
- **Access:** [OAuth scope / skill name]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Read and search freely.
  - Drafting in Docs is fine; sharing externally requires permission.
  - Gemini in-product summaries are a sanity layer, not a memory substitute.

## Slack

- **Workspace:** [workspace name]
- **Account:** [username or email]
- **Access:** [OAuth scope / skill name]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Read all channels and DMs freely.
  - Never send messages without permission.
  - In group channels: observe, don't participate unless asked.
  - DMs: draft responses for review.

## Notion

- **Workspace:** KRING Ventures
- **Access:** [OAuth scope / skill name]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Read and search freely.
  - Modify pages only with **explicit per-action permission**. Never touch pages owned by another Speedblock owner without go-ahead.
  - **Never rename a Notion page.** Scope shifts → next sequential version.
  - Log decisions into the PM Tasks DB **as they land**, one at a time.
  - Keep task Status live as work moves.

## GitHub

- **Account:** [username]
- **Access:** [OAuth scope / skill name]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Read repos freely.
  - Pushing, PRs, or issue comments require permission.
  - CodeRabbit handles review on Cosmica; don't override.

## Telegram (OP surface)

- **Account / chat:** [@handle or chat ID]
- **Access:** [bot token / harness config]
- **Status:** ❌ Not yet connected
- **Rules:**
  - Primary surface — wire first.
  - Parse dictated / messy messages for intent; don't ask for rephrasing.
  - Never forward Telegram content to other surfaces without explicit instruction.

## Workspace files

- **Primary workspace:** `{{WORKSPACE_PATH}}`
- **Access:** Local
- **Status:** ✅ Connected
- **Rules:**
  - Organise freely within the workspace.
  - Ask before modifying files outside the workspace.
  - Use `trash/` over `rm`.

## Web

- **Browser access:** via OpenClaw harness (WebFetch, WebSearch, browser skill).
- **Status:** ✅ Available
- **Rules:**
  - Search freely for research and context.
  - Don't fill out forms or create accounts without permission.
  - Don't access anything requiring {{USER_FIRST_NAME}}'s credentials without instruction.

---

## Adding new tools

When connecting a new tool:
1. Fill in the section above (or create a new one).
2. Update the connection status table at the top.
3. Test the connection.
4. Log in `MEMORY.md` that the tool was connected and when.

Template:

```markdown
## [Tool name]
- **Purpose:** [what it's for]
- **Access:** [how to use it]
- **Status:** [✅ Connected / ❌ Not connected]
- **Rules:** [specific constraints]
```
