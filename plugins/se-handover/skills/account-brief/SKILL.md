---
name: account-brief
description: Answers questions about an inherited customer account from the handover knowledge base in cloud storage — context, contacts, open items, history, environments, and what the previous owner thought of it. Use when someone asks "what's open on Acme", "who do we talk to at Acme", "catch me up on Acme", "what did the previous owner say about Acme", "what must I not do with Acme", "brief me on Acme", or any question about an account listed in the handover 00_START_HERE.
---

# Account brief

Answer from the handover knowledge base, with sources, in English.

## Locate the knowledge base
1. Find `00_START_HERE` in ~~cloud storage (search by title; if several, ask which handover). Read it once per session: it holds the reading rules and the account index with folder and document IDs.
2. Resolve the account name against the index (aliases, former names). If it is not in the index, say so and stop — do not answer from general knowledge.

## Answer
1. Read only the documents the question needs:
   - who / what / where / environments / channels → `00_README`
   - what happened / when / have we already → `01_HISTORY`
   - what's open / who owns / is the customer waiting / dates / promises / risks → `02_OPEN_ITEMS`
   - what did the previous owner think / how to handle / next steps / what not to do → `03_OWNER_NOTES`
   - "catch me up" → all four, in order.
   If a document ID fails, search the account folder by title.
2. Lead with the direct answer, then the supporting facts each with the source the document gives, then one line on unknowns ("not in the handover — check ~~chat").
3. State freshness: the "researched on" date of the documents. For anything newer, offer to check ~~chat or ~~email if connected.
4. Distinguish voices: the Sentiment paragraph is the previous owner's own words; "(from sources)" lines are research inferences.

## Guardrails
- Never guess; "not found" in a document means it was looked for.
- Commercial figures: add "confirm with the account manager before quoting to the customer".
- Read-only: never post, email, or edit documents here — updates go through `log-update`.
- If ~~cloud storage is not connected, say the handover lives there and must be connected; do not answer from memory.
