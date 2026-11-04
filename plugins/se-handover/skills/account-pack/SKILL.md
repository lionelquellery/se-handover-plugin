---
name: account-pack
description: Researches one or more customer accounts across chat, email, CRM, call recordings, tickets and the product admin, and writes a sourced four-document handover pack per account (README, HISTORY, OPEN_ITEMS, OWNER_NOTES). Use when someone says "build the handover pack for Acme", "document my accounts for my successor", "research Acme for the handover", "create the account fiches", "we forgot Acme in the handover folder".
---

# Account pack

Read `references/conventions.md` and `references/pack-templates.md` before starting. Follow them exactly.

## Inputs
- Account name(s). For each: account manager, interim owner, urgency and the owner's sentiment if already captured (from `sentiment-interview` or the user). Missing sentiment → "Not captured"; offer to run the interview.
- Optional baseline: an existing handover plan or older notes — reuse vetted facts, then update.

## Research (read-only)
For each account:
1. **~~chat** — find the customer shared channel and the internal account channel (search channel names and variants: former company names, parent company, product names). Read the full history; denser on the last 12 months. Search escalation / support channels for threads naming the account.
2. **~~email** — search by company name, domain, product and parent-company names. Skip calendar and notification noise but use call-recording notifications for call dates. Some customers work almost only by email: if chat is thin, weight email higher.
3. **~~product admin** — environments / workspaces with IDs and region, configuration inventory, usage vs contract, failing jobs or alerts.
4. **~~CRM** — ARR, renewal date, term, open opportunities, owners.
5. **~~call recorder** — list key calls (date, title, attendees); read transcripts only for the 1–2 decisive calls.
6. **~~project tracker** — open bugs and feature requests linked to the account.
7. **~~knowledge base** — account pages; treat as a possibly stale snapshot.
If a connector is missing, note it under "sources not accessible" and continue.

For several accounts, run parallel sub-agents (3–4 accounts each). Give each sub-agent the two reference files, the account facts above, and the instruction to write files only — no posting, no drafts.

## Write
Produce the four documents per account from `references/pack-templates.md`. Keep the Sentiment paragraph exactly as captured. Make risk signals explicit when the owner says the account is at risk.

## Hand-back to the user
Per account: the most important findings (≤8 bullets), sources not accessible, and facts the owner must check. Collect the "must check" items for `99_FACTS_TO_VERIFY`. Then propose `knowledge-base-publish`.
