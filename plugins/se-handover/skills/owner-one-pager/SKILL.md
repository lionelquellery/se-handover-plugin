---
name: owner-one-pager
description: Produces a one-page handover summary for a manager or account manager / CSM covering only their accounts — one table with account, interim owner, owner if a hire arrives, hot topics and the departing owner's sentiment. Use when someone says "make a one-pager for my manager", "summary for Sarah's accounts", "the plan is too long, give me one page", "condensed handover table", "one-pager per account manager".
---

# Owner one-pager

Managers do not read 30 pages. Give them one table they can act on.

## Procedure
1. Identify the recipient and their accounts (from the knowledge base `00_START_HERE`, the handover plan, or ~~CRM ownership). Confirm the list.
2. For each account, collect:
   - **Interim owner (no hire)** and **owner if a new hire arrives** — from the plan; if undecided, ask with AskUserQuestion (one panel); otherwise write "to confirm".
   - **Hot topics** — 2–4 short phrases from `02_OPEN_ITEMS` (customer-waiting items first), or from a fresh scan of the last 30 days of ~~chat if no pack exists. Plain words if the recipient is not technical.
   - **Sentiment** — the owner's words only (from `sentiment-interview` or `03_OWNER_NOTES`). If missing, leave "to fill" visibly and ask the owner; never invent it.
   - **Urgency** — High / Medium / Low, consistent with the sentiment (flag mismatches to the owner, e.g. "at risk" tagged Low).
3. Layout: title, one subtitle line (from → to, date, last day), then the table: Account · Interim · If new hire · Hot topics · Sentiment. One line under the table: "Hot topics as of <date> — some may have closed since."
4. Render to a single landscape page (PDF or the user's document tool). If it overflows, shorten hot topics, never drop accounts.
5. Show it to the owner for review before it goes anywhere.

## Guardrails
- One page, no paragraphs of prose.
- Commercial figures only if sourced; mark "confirm with account manager".
- Do not send it; the owner shares it.
