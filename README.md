# SE Handover — a Claude plugin

Prepares a Solutions Engineer (or any post-sales technical owner: TAM, SA, CSE) to hand over their customer accounts, and gives the successor a knowledge base they can query with Claude.

## Install

In Claude Code or Cowork:

```
/plugin install se-handover --marketplace lionelquellery/se-handover-plugin
```

or in two steps:

```
/plugin marketplace add lionelquellery/se-handover-plugin
/plugin install se-handover@se-handover-plugin
```

The repository is private for now: you need read access to it for the install to work.

Then customize it once for your company ("customize the se-handover plugin") so the `~~` tool placeholders map to your stack — see [`plugins/se-handover/CONNECTORS.md`](plugins/se-handover/CONNECTORS.md).

## What's inside

| For the person leaving | For the successor |
|---|---|
| `handover-plan` — inventory, interim vs new-hire ownership, timeline, customer comms | `account-brief` — answer any question about an account, with sources |
| `sentiment-interview` — capture the owner's judgment, account by account | `call-prep` — one-screen brief before a customer meeting |
| `account-pack` — 4 sourced docs per account: README, HISTORY, OPEN_ITEMS, OWNER_NOTES | `portfolio-view` — risk, customers waiting, upcoming dates |
| `knowledge-base-publish` — one folder per account + START_HERE index + FACTS_TO_VERIFY | `log-update` — dated, sourced entries that keep the base alive |
| `owner-one-pager` — one page per manager / account manager | |

Full documentation: [`plugins/se-handover/README.md`](plugins/se-handover/README.md).

## Repository layout

```
.claude-plugin/marketplace.json   # marketplace manifest
plugins/se-handover/              # the plugin
  .claude-plugin/plugin.json
  CONNECTORS.md                   # tool categories to map to your stack
  README.md
  skills/<skill>/SKILL.md         # nine skills
```
