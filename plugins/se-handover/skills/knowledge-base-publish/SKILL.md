---
name: knowledge-base-publish
description: Publishes the handover account packs into a queryable knowledge base in cloud storage — one folder per account with its four documents, a 00_START_HERE index that tells Claude and humans how to read it, and a 99_FACTS_TO_VERIFY checklist. Also adds or refreshes a single account later. Use when someone says "put the handover in Drive", "publish the knowledge base", "upload the account packs", "create the handover folder", "add Acme to the handover folder", "refresh the start-here index".
---

# Knowledge base publish

Read `../account-pack/references/conventions.md` and `../account-pack/references/pack-templates.md`.

## Procedure
1. **Locate the root folder** in ~~cloud storage (ask for the link if not given). List what already exists: account folders, existing documents, older files. Never delete or move the user's existing files.
2. **Folders** — one per account, named after the account. Reuse an existing folder when the name matches (case-insensitive, aliases); create only the missing ones.
3. **Documents** — upload each pack document as a native document of the storage tool (e.g. a Google Doc converted from markdown), titled `00_README`, `01_HISTORY`, `02_OPEN_ITEMS`, `03_OWNER_NOTES`. Upload content verbatim.
4. **Replacing a document** — if the storage tool cannot edit document content in place: create the new version first, verify it, then move the old one to the trash (never permanent delete). Record the new IDs.
5. **00_START_HERE** at the root — follow the template. Its account index table must include the folder ID and the four document IDs per account: the successor skills (`account-brief`, `call-prep`, `portfolio-view`, `log-update`) navigate from this table. Regenerate it whenever an account is added or a document is replaced.
6. **99_FACTS_TO_VERIFY** at the root — every unconfirmed fact, grouped by account, plus sources not accessible.
7. **Verify** — read back one document per type through the connector and run one full-text search for a distinctive term, to confirm the content is indexed and readable by a future Claude session.
8. **Report** — links to the root, START_HERE and FACTS_TO_VERIFY, the list of folders created vs reused, and any failure.

## Sharing
Tell the user who needs access (successor, interim owners, account managers) and that the successor skills require the ~~cloud storage connector with access to this folder. Do not change sharing settings unless asked.

## Guardrails
- Ask before overwriting or trashing anything.
- Do not upload raw research dumps or scratch files.
