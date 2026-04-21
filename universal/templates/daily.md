# Daily Morning Brief — Template

Runs Mon-Fri at the user's configured start-of-day time (from USER.md §Patterns).

## Rendering rules

- Short. Telegram-readable on a phone. No preamble, no "Good morning!" — just the brief.
- Use the user's voice conventions from USER.md §Voice.
- Skip any section that's genuinely empty (don't render "No urgent emails." if there are none — skip the section).
- Tag urgency honestly — don't inflate. "Important" ≠ "Urgent."
- End with one concrete suggestion, not "have a great day."

## Structure

```
📅 {DAY}, {DATE}

**Calendar**
• {time} — {event title} ({with whom if relevant, else omit})
• {time} — {event title}
→ {one-line prep note if needed, else omit}

**Inbox**
Urgent ({n}):
• {sender} — {one-line subject/gist} → {what they're asking for}
Important ({n}):
• {sender} — {one-line subject/gist}
Open threads waiting on you ({n}):
• {thread} — last msg {relative time} ago

**Tasks & reminders**
Due today:
• {task}
Overdue:
• {task} — {how overdue}

**One thing worth noticing**
{A pattern, blocker, or opportunity the user might miss. Optional — omit if nothing worth saying.}
```

## Data sources

- Calendar: Google Calendar (OAuth scope in TOOLS.md).
- Inbox: Gmail primary + important labels. Skip promotional/social. Urgency heuristic:
  - Urgent = direct to user, time-critical language, or from flagged-critical contacts (list in USER.md §People).
  - Important = flagged or from §People priority contacts.
- Tasks: Notion tasks DB (user's personal) + Google Tasks if connected.

## What not to do

- No motivational quotes.
- No emoji-stuffing. One calendar emoji, done.
- Don't summarise the whole inbox — only things that need the user's attention.
- Don't predict how the day will go. Just show what's on it.
