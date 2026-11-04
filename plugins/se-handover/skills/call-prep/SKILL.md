---
name: call-prep
description: Prepares a one-screen pre-call brief for a meeting with an inherited customer account, combining the handover pack (open items, previous owner's guidance, do-not list) with recent chat and calendar activity. Use when someone says "prep me for my Acme call", "I have a sync with Acme tomorrow", "call prep Acme", "what should I know before meeting Acme", "agenda for the Acme quarterly".
---

# Call prep

## Procedure
1. Locate `00_START_HERE` in ~~cloud storage and resolve the account (same as `account-brief`).
2. Read `02_OPEN_ITEMS` and `03_OWNER_NOTES` (always), `00_README` (contacts, cadence), and the last 3 months of `01_HISTORY`.
3. If ~~chat is connected: read the customer and internal channels named in `00_README` since the pack's "researched on" date (max 30 days). Read-only.
4. If ~~calendar is connected and a meeting is named: pull time and attendees.
5. If ~~email is connected and the account works by email: check the last 14 days of threads with the customer domain.

## Output (one screen)
- **Account · meeting · attendees (us / them)**
- **Where things stand** — 3–5 bullets with sources; customer-waiting items first.
- **Since the handover** — what changed in chat/email; or "not checked — pack dated <date>".
- **Previous owner's guidance** — Sentiment (quoted) + the relevant "do not" lines.
- **Suggested agenda** — 3–4 points from open items; commercial topics last, flagged "with account manager".
- **Unknowns** — facts marked "not found" that the meeting may touch.

## Guardrails
- No agenda item that is not grounded in open items or recent activity.
- Nothing is sent anywhere; this is a brief for the user.
