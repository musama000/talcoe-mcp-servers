# Public Meeting Agendas MCP server

Ask: "What contracts are on Denver's committee agendas this week?"

One of the rows that comes back:

```json
{
  "platform": "legistar",
  "jurisdiction": "Denver",
  "state": "CO",
  "body": "Health and Safety",
  "meetingDate": "2026-11-25T10:30:00",
  "itemTitle": "Approves a contract with JKS Industries LLC for $7,500,000.00 with an end date of 12-31-2030 for asbestos removal and regulated building material abatement ...",
  "matterType": "Resolution"
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/public-meeting-agendas,talcoe/boarddocs-agendas
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--public-meeting-agendas` | Agenda items from city councils, county boards and school boards on Legistar, BoardDocs and CivicClerk, filtered by jurisdiction, keyword and date window | $0.005 per item |
| `talcoe--boarddocs-agendas` | School board agenda items from BoardDocs portals, filtered by district, committee, date range and keyword, with optional item text and attachment links | $0.015 per item |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "What contracts are on Denver's committee agendas this week?"
- "Search school board agendas for cell phone policy items in the last 30 days."
- "Which county boards have solar farm permits on their agendas this month?"

## Source actors

- [Public Meeting Agendas: City Council, County, School Board](https://apify.com/talcoe/public-meeting-agendas)
- [BoardDocs School Board Agendas Scraper by District](https://apify.com/talcoe/boarddocs-agendas)
