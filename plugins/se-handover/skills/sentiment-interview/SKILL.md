---
name: sentiment-interview
description: Interviews the departing Solutions Engineer account by account to capture their personal sentiment and judgment — relationship health, champions, real risks, real opportunities, advice for the successor — using quick multiple-choice panels. Use when someone says "interview me about my accounts", "capture my sentiment", "ask me questions about each account", "my handover lacks my opinion", "what do I think of each customer", or after a handover plan is built.
---

# Sentiment interview

The facts can be researched; the owner's judgment cannot. Capture it fast, in their words.

## Procedure
1. Get the account list (from the handover plan, the knowledge base `00_START_HERE`, or ask).
2. For each account, prepare context first: skim the account's open items or the last 60 days of ~~chat so the options are specific (name the real champion, the real open topic).
3. Ask with AskUserQuestion — **one account per question, up to 4 accounts per panel**, so the user can chain answers quickly. Each question offers 2–4 concrete stances, for example:
   - "Solid, key account" · "Good but demanding" · "To watch" · "At risk"
   - or account-specific: "Champion strong — a strength" · "Champion leaving — risk" · "Growth opportunity on <topic>"
   The user can always type a free answer instead; prefer theirs.
4. After the sentiment round, run one panel for decisions still open: interim owner per account (or "same for all"), urgency corrections.
5. If an answer is thin, ask at most one follow-up for that account (what the successor must do / must not do). Accept "nothing to add".
6. Read back a compact table (account · sentiment in the owner's words · interim owner) and ask for corrections.

## Output
- Store the sentiment lines so `account-pack` and `owner-one-pager` can use them verbatim (keep them in the conversation, and in the knowledge base `00_START_HERE` index if it exists — via `log-update` rules: show text, confirm, then write).
- Translate to English if the user answered in another language, keeping the meaning; show the translation for approval.

## Guardrails
- Never invent a sentiment. If the user skips an account, write "Not captured".
- Do not soften or sharpen what the user said.
- Keep personal opinions about named customer individuals professional; drop anything that is not about how they work with us.
