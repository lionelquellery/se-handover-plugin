# Account pack templates

Four documents per account, in one folder named after the account. Header line of each file: `# <Account> — <document name> (researched on YYYY-MM-DD)`.

## 00_README — start here for the account
- **Summary** — one paragraph: who the customer is, what they do with our product, how long they have been a customer.
- **Commercial** — ARR, plan/tier, contract volume, term, renewal date, signatory. Each with source or "not found".
- **Our team** — account manager / CSM, AE, outgoing owner → interim owner → future owner, engineers on active threads and what they own.
- **Customer contacts** — table: name · role · what they own · how they work (responsive? technical? sensitive to what?) · channel they use. Only what sources show.
- **Partners / agencies** involved, and their role.
- **Channels** — customer shared channel (name + ID), internal channel (name + ID), email distribution, other relevant channels.
- **Environments** — workspaces / tenants / projects: name, ID, region, environment (prod/dev/staging). Flag IDs that only come from a stale source.
- **Stack / configuration** — what they use from our product, main integrations, custom code (transformations, scripts), features in beta.
- **Recurring meetings** — name, cadence, organiser, attendees.
- **Key files** — decks, reports, questionnaires, diagrams: title + link.

## 01_HISTORY — chronology
Reverse-chronological list. Each entry:
`**YYYY-MM-DD** · what happened · outcome · source`
Cover incidents, escalations, projects, feature requests, decisions, security/legal reviews, commercial milestones. Go as far back as sources allow; denser for the last 6 months.
End with **Patterns** — 3–5 bullets on what kind of issue recurs on this account.

## 02_OPEN_ITEMS — what is live today
1. Table: item · our owner · customer counterpart · status / last update (date) · customer waiting on us? (Yes/No) · source. Items where the customer is waiting go first.
2. **Dates the successor inherits** — meetings, renewals, deadlines, events, executive visits.
3. **Commitments made in the outgoing owner's name** — anything promised that must be re-owned by name.
4. **Waiting on the customer** — what we asked them and have not received.
5. **Recently closed** — so nobody re-opens it.
6. **Risk signals** — usage vs contract, unanswered outreach, champion departures, incidents, competitor mentions, cost-cutting. Each sourced; if none are visible, say so.

## 03_OWNER_NOTES — the human part
1. **Sentiment (owner)** — the owner's words from the sentiment interview, lightly polished, meaning unchanged. If no interview happened: "Not captured."
2. **What the new owner must know** — technical patterns not to change, sensitivities, how the customer likes to be answered, bot/automation caveats.
3. **What I would do next** — 2–3 concrete next steps.
4. **Do not** — short list of mistakes to avoid.
Maximum one page. Label every line "(owner)" or "(from sources)".

## Root documents of the knowledge base
- **00_START_HERE** — purpose, folder layout, reading rules (conventions summary), freshness date, account index table (account · account manager · interim owner · urgency · sentiment one-liner · folder ID · four doc IDs), people who recur across accounts, how to use it with Claude.
- **99_FACTS_TO_VERIFY** — per account, everything research could not confirm; sources that were not accessible.
