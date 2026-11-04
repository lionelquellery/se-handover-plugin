# Handover conventions (shared by every skill in this plugin)

## Truthfulness
- Every non-trivial fact carries its source: a ~~chat permalink, an ~~email (subject · date · sender · link), a ~~call recorder call (date · title), a ~~CRM record, a ~~project tracker ticket ID, or a ~~product admin tool + object ID.
- If something was looked for and not found, write **"not found"**. Never fill a gap with a plausible guess, and never reuse content from another account.
- Commercial figures (ARR, renewal date, contract volume) are quoted only from ~~CRM or where a person stated them in writing. When they come from chat or a call, say so and add "confirm with the account manager before quoting to the customer".
- Date everything. Use ISO dates (YYYY-MM-DD); UTC for times when they matter.

## Voice labels in the notes file
- The **Sentiment** paragraph of `03_OWNER_NOTES` is the outgoing owner's own words, captured in the sentiment interview. It is never rewritten by anyone else.
- Lines drawn from sources by Claude are prefixed **"(from sources)"**.
- Lines the outgoing owner stated outside the Sentiment paragraph are prefixed **"(owner)"** — only if they actually said it.

## Source reliability (highest first, adapt per company)
1. ~~chat customer channel and internal account channel
2. ~~email threads with the customer
3. ~~product admin (live configuration and usage)
4. ~~CRM (commercial facts)
5. ~~call recorder (what was said on calls)
6. ~~knowledge base / internal trackers (often stale — treat as a snapshot)

## Bots and automation
If an AI assistant or bot answers in customer channels, record cases where it was wrong, and remind readers that a human verifies bot answers before the customer relies on them. Record any automation the outgoing owner runs (trackers, digests, alerts routed to them) — it stops or goes stale when they leave.

## Read-only research
Research never posts, reacts, drafts, labels, archives, edits tickets or changes product configuration. Writes happen only in the knowledge base, and only through `knowledge-base-publish` or `log-update`, after the user confirms.

## Language
Write deliverables in English unless the user asks for another language.

## Privacy
Customer contact details and commercial figures stay internal. Do not include personal or sensitive information about individuals beyond their work role and how they work with the company.
