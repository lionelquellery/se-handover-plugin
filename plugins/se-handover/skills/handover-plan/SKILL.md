---
name: handover-plan
description: Builds the overall handover plan for a departing Solutions Engineer (or any post-sales technical owner) — account inventory, who takes each account in two scenarios (interim vs new hire), what the owner must close before their last day, a week-by-week timeline, and a customer communication plan. Use when someone says "I'm leaving, help me plan my handover", "prepare my account handover", "build a transition plan for my accounts", "who should take my accounts", "offboarding plan for my portfolio", or "my last day is 30 Nov".
---

# Handover plan

Produce the master plan the rest of the plugin builds on. Read `../account-pack/references/conventions.md` first and follow it.

## 1. Gather the frame (ask, don't assume)
Use AskUserQuestion, at most 4 questions per panel:
- Last day (and whether it is official — nothing goes to customers before it is).
- Who receives the plan (manager, account managers / CSMs, successor).
- Known interim owner(s) and whether a hire is planned.
- Where the knowledge base will live in ~~cloud storage (folder link).

## 2. Inventory the accounts
Build the list from, in order: the user's own list; ~~CRM accounts where the user is the technical owner; ~~chat customer channels the user belongs to; ~~calendar recurring customer meetings. Show the merged list with its source and ask the user to confirm, remove or add accounts. Record the account manager / CSM for each.

## 3. Quick scan per account
For each confirmed account, scan the last 60 days of ~~chat (customer + internal channel) and ~~email, plus ~~calendar for upcoming meetings. Extract: items where the customer is waiting on us, commitments in the user's name, upcoming dates, active engineers. For more than ~5 accounts, delegate the scan to parallel sub-agents, one per 3–4 accounts, each read-only.

## 4. Write the plan
Sections, in this order:
1. **Header** — owner, last day (official or expected), recipients, sources consulted, caveats (sources not accessible).
2. **Ownership** — table: account · urgency (High / Medium / Low / Decision) · current owner · interim owner (no hire) · owner if a new hire arrives (wave 1 = live technical work, wave 2 = quieter / renewal-driven) · engineers who stay on · why. List open ownership decisions separately.
3. **Timeline** — week by week to the last day: agree the plan → introduce interim owners and close loose ends → transfer calendars, channels and tooling → final status per account. Then the dates after the last day that owners inherit.
4. **Customer communication plan** — ground rules (nothing before the date is official; the account manager sends, the departing owner replies in-thread; one message per channel; name the new contact; no new promises), suggested wording, and per account: where/when, addressed to, introduces, notes.
5. **What customers are waiting on today** — table with "waiting since" and who answers.
6. **Close-out checklist** — grouped: answer now · close or park explicitly · transfer commitments made in the owner's name · one written brief per internal channel · calendar, channels, wiki and tooling. Each line with a target date.
7. **Tooling that depends on the owner** — automations, bots, alert routing, recurring invites, files only they hold.

## 5. Deliver
Create the plan as a document in the user's preferred format (ask: doc, PDF, or ~~cloud storage doc). Keep per-account detail out of the plan — that belongs in `account-pack`. End by proposing the next steps: `sentiment-interview`, then `account-pack` for each account, then `knowledge-base-publish` and `owner-one-pager`.

## Guardrails
- Never message customers or colleagues; draft only, and only when asked.
- Mark every inferred ownership proposal as a proposal for the manager to confirm.
