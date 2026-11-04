---
name: portfolio-view
description: Gives a cross-account view of an inherited portfolio from the handover knowledge base — accounts at risk, customers waiting on us, upcoming renewals and dates, who owns what. Use when someone asks "which accounts are at risk", "what's waiting on us across my accounts", "renewals coming up", "what do I inherit", "status of Sarah's accounts", "weekly portfolio check".
---

# Portfolio view

## Procedure
1. Read `00_START_HERE` in ~~cloud storage for the account index (account manager, interim owner, urgency, sentiment, document IDs).
2. Scope: filter by account manager, owner, urgency or named accounts if the user asks; otherwise all accounts. Tell the user how many documents will be read.
3. For each account in scope, read `02_OPEN_ITEMS` (in parallel where possible). Extract: customer-waiting items and their age; dates in the window (default next 60 days); commitments from the previous owner not yet re-owned; risk signals.
4. For "at risk": combine the previous owner's sentiment, customer-waiting items older than 7 days, and the risk-signal section.

## Output
- One line at the top: knowledge base freshness date.
- Table: Account · Account manager · Owner · Urgency · Customer waiting (count + oldest) · Next date · One-line status. Sorted by urgency, then oldest waiting item.
- 3–5 bullets "what I would do this week", each tied to a row and its source document.
- Unknowns: accounts whose documents mark the relevant fact "not found".
- Offer a ~~chat refresh per account through `call-prep`.

## Guardrails
- Commercial figures: "confirm with the account manager".
- Read-only.
