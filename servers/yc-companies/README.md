# Y Combinator Companies MCP server

Ask: "Which Winter 2025 companies in industrials are hiring?"

One of the rows that comes back:

```json
{
  "name": "Red Barn Robotics",
  "batch": "Winter 2025",
  "status": "Active",
  "teamSize": 5,
  "industry": "Industrials",
  "oneLiner": "A Roomba for weeds on a farm.",
  "website": "https://www.redbarnrobotics.com",
  "location": "Seattle, WA, USA",
  "isHiring": false
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/yc-companies
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--yc-companies` | Companies in the Y Combinator directory by keyword, batch, industry, status or hiring, with team size, location and tags | $0.005 per company |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "Which Winter 2025 companies in industrials are hiring?"
- "List active YC fintech companies in New York with more than 50 people."
- "Find YC companies working on farm robotics."

## Source actor

- [Y Combinator Companies Scraper](https://apify.com/talcoe/yc-companies)
