# SE Handover

A plugin that prepares a Solutions Engineer — or any post-sales technical owner (TAM, SA, CSE) — to hand over their customer accounts properly, and gives their successor a knowledge base they can actually query.

Built from a real handover of ~20 enterprise accounts: the facts can be researched by Claude; the owner's judgment has to be captured before they leave. This plugin does both.

## How it works

```
OUTGOING OWNER                                        SUCCESSOR / TEAM
handover-plan ──► sentiment-interview ──► account-pack ──► knowledge-base-publish ──► account-brief
                                                      └──► owner-one-pager           call-prep
                                                                                     portfolio-view
                                                                                     log-update
```

### For the person leaving
| Skill | What it does | Try saying |
|---|---|---|
| `handover-plan` | Account inventory, interim vs new-hire ownership, timeline to the last day, customer comms plan, close-out checklist | "My last day is 30 Nov — plan my handover" |
| `sentiment-interview` | Quick multiple-choice panels, one account per question, to capture your judgment of each account | "Interview me about my accounts" |
| `account-pack` | Researches each account (chat, email, CRM, calls, tickets, product admin) and writes 4 sourced docs: README, HISTORY, OPEN_ITEMS, OWNER_NOTES | "Build the handover pack for Acme" |
| `knowledge-base-publish` | Puts everything in cloud storage: one folder per account, a 00_START_HERE index, a 99_FACTS_TO_VERIFY checklist | "Publish the handover to our Drive folder" |
| `owner-one-pager` | One landscape page per manager / account manager: interim owner, hot topics, your sentiment | "One-pager for my CSM's accounts" |

### For the successor and the team
| Skill | What it does | Try saying |
|---|---|---|
| `account-brief` | Answers any question about an account, with sources | "What's open on Acme?" |
| `call-prep` | One-screen brief before a customer meeting, with recent chat activity | "Prep me for my Acme quarterly" |
| `portfolio-view` | Cross-account table: risk, customers waiting, upcoming dates | "Which accounts are at risk?" |
| `log-update` | Adds dated, sourced entries so the knowledge base stays alive | "Log on Acme: SSO issue fixed today" |

## Principles baked into every skill
- **Every fact has a source** (chat permalink, email, call, CRM record, ticket, admin ID). "Not found" means it was looked for — no guessing.
- **The owner's voice is protected**: the Sentiment paragraph is their words; everything inferred is labelled "(from sources)".
- **Read-only research.** Nothing is posted, emailed or changed in your tools. Writes happen only in the knowledge base, after confirmation, and nothing is permanently deleted.
- **Commercial figures** are flagged "confirm with the account manager".

## Setup
1. Install the plugin.
2. Customize it once for your company (ask Claude: "customize the se-handover plugin") so the `~~` placeholders become your real tools — see `CONNECTORS.md`.
3. Connect at least **cloud storage**; chat, email, calendar and CRM make the packs much richer.
4. Outgoing owner: start with `handover-plan`. Successor: connect the same cloud storage folder and start with `account-brief`.

## Tips from the field
- Start 3–4 weeks before the last day; customers should hear about the change only once it is official.
- Run the sentiment interview early — managers consistently ask for the owner's opinion, not just the facts.
- Some customers live in email, not chat: check both before calling a pack complete.
- Re-check the packs a few days before leaving; anything from 99_FACTS_TO_VERIFY you can answer from memory is worth more than another hour of research.
