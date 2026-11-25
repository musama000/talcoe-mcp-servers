# US Business Entities MCP server

Ask: "List plumbing LLCs formed in Colorado this month."

One of the rows that comes back:

```json
{
  "state": "CO",
  "entityName": "Thor Plumbing LLC",
  "entityId": "20268373296",
  "entityType": "DLLC",
  "status": "Good Standing",
  "formationDate": "2026-11-08",
  "city": "Lafayette"
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/us-business-entity-search
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--us-business-entity-search` | Business registry records from Colorado, New York, Oregon and Connecticut in one schema, filtered by name, city, entity type, status and formation date, with entity id, registered agent and addresses | $0.004 per record |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "List plumbing LLCs formed in Colorado this month."
- "Is there an active company named Cascade Roofing in Oregon, and when was it formed?"
- "Find corporations formed in Hartford, Connecticut this year."

## Source actor

- [US Business Entity Search: CO, NY, OR, CT State Registries](https://apify.com/talcoe/us-business-entity-search)
