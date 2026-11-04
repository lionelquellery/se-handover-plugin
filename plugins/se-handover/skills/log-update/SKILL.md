---
name: log-update
description: Keeps the handover knowledge base alive by adding a dated, sourced entry to an account's HISTORY or OPEN_ITEMS document (or a lesson to OWNER_NOTES) after something happens — an incident, a call, a decision, an item opened or closed. Use when someone says "log this on Acme", "add to the Acme history", "mark the SSO issue as closed", "update the open items for Acme", "note that we promised X to Acme", or pastes a chat thread and asks to record it.
---

# Log update

Writes are allowed only after the user confirms the exact text.

## Procedure
1. Locate `00_START_HERE` in ~~cloud storage and resolve the account and document IDs.
2. Choose the target:
   - something happened → `01_HISTORY`
   - an item opened, changed owner or closed → `02_OPEN_ITEMS` (plus a one-line `01_HISTORY` entry for meaningful decisions)
   - a lasting lesson about handling the customer → `03_OWNER_NOTES`, under a heading "Added after handover"
3. If the user pasted a ~~chat link or an ~~email, read it to get the facts and the link. Read-only.
4. Read the current document and place the entry:
   - `01_HISTORY`: at the top, `**YYYY-MM-DD** · what happened · outcome · source`
   - `02_OPEN_ITEMS`: new table row, or move the row to "Recently closed" with date and source.
5. Show the exact text and its position; ask one confirmation question. No write before a yes.
6. Write through the ~~cloud storage connector. If it cannot edit content in place, create the new version, verify it, trash the old one (never permanent delete), and update the document ID in `00_START_HERE` the same way.
7. Append `(added by <user>, YYYY-MM-DD)` to the entry. Confirm with the document link.

## Guardrails
- Only add, or move an item to Closed. Never rewrite or delete existing entries.
- Never change the previous owner's Sentiment paragraph.
- Every entry has a source; if none, write "source: <user>, verbal".
- If a document is missing, tell the user instead of creating a new structure.
