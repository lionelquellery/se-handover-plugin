# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. The skills describe the handover workflow in terms of categories rather than specific products, so the plugin works whatever stack your company uses. Customize the plugin once for your company to replace the placeholders with your real tools.

## Connectors for this plugin

| Category | Placeholder | Typical options | Used for | Required? |
|---|---|---|---|---|
| Cloud storage | `~~cloud storage` | Google Drive, SharePoint / OneDrive, Box, Dropbox | Where the handover knowledge base lives; successor skills read and update it | **Yes** |
| Chat | `~~chat` | Slack, Microsoft Teams, Discord | Customer shared channels, internal account channels, escalation threads — the primary research source | Strongly recommended |
| Email | `~~email` | Gmail, Outlook | Customers who work by email; contracts, security reviews, renewals | Recommended |
| Calendar | `~~calendar` | Google Calendar, Outlook Calendar | Recurring customer meetings to transfer; call prep attendees | Recommended |
| CRM | `~~CRM` | Salesforce, HubSpot, Pipedrive | ARR, renewal dates, contract terms, account owners | Recommended |
| Call recorder | `~~call recorder` | Gong, Chorus, Zoom AI, Fireflies, Avoma | Decisive calls, commitments made out loud | Optional |
| Ticketing / tracker | `~~project tracker` | Jira, Linear, Zendesk, Plain, ServiceNow | Bugs, feature requests and support tickets tied to an account | Optional |
| Internal wiki | `~~knowledge base` | Notion, Confluence, Guru | Account pages, runbooks, internal trackers | Optional |
| Product admin | `~~product admin` | Your own product's admin API / MCP server | Workspace IDs, configuration inventory, usage vs contract | Optional |

A skill that needs a category that is not connected says so and carries on with the sources it has; it never fills the gap with guesses.
