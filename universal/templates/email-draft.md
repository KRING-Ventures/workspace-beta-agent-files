# Email Draft — Template & Pattern

How the agent drafts emails on the user's behalf. Voice is pulled from USER.md §Voice at render time. Structure is universal.

## Draft rules

- **Draft only.** Never send. Return the draft to the user for approval and edit.
- **Match the user's voice** (see USER.md §Voice). If voice not yet captured (USER.md §Voice empty), flag "voice not yet calibrated — please review carefully" at the top of the draft.
- **Shortest reasonable length.** Err on the side of brevity. The reader's time matters.
- **No AI-tells.** No "I hope this email finds you well." No "I wanted to reach out regarding..." No "kindly." Plain openers: recipient's name, then the thing.
- **No em dashes unless the user uses them** (check USER.md §Voice).

## Output format to user

When returning a draft in Telegram, use this shape:

```
📧 Draft → {recipient name}
Subject: {subject line}

{body}

---
Reply "send" to send as-is, "edit: {your change}" to change, or just paste a new version.
```

## Body structure (default)

For most emails:

1. **Context line** (one sentence, if needed — what this is about)
2. **The ask / point** (what you want the reader to do, or what you're telling them)
3. **Details** (only what they need to act on the ask)
4. **Close** (one line — next step or "let me know" — no "best regards" unless the user uses them)

## Reply to inbound — common patterns

### Reply declining
- Acknowledge the ask.
- Decline clearly — no hedging, no "I wish I could."
- Offer alternative if there is one.
- Close.

### Reply agreeing / committing
- Confirm the ask as you understood it.
- State your commitment (what, by when).
- One line on what you need from them, if anything.

### Reply needing more info
- One sentence: here's what I need to proceed.
- Frame the question specifically — don't dump all possible questions.

### Reply saying "not now / not me"
- Brief explanation (one sentence).
- Redirect if possible (to a person or a later time).

## Outbound — asking for something

- State the ask in the first sentence.
- Give context in the second.
- Make it easy to say yes (specific enough that the recipient doesn't have to ask follow-ups).
- Deadline if relevant.

## Never draft without flagging

- If the email is to someone **not in USER.md §People** and the user hasn't emailed them before — flag: "First email to this recipient — review tone carefully."
- If the email **breaks a commitment** (saying no to something the user previously said yes to) — flag it.
- If the email touches **legal, HR, financial** matters — flag and suggest the user write this one themselves or review extra carefully.
