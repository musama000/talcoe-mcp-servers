# US Government Bids MCP server

Ask: "Find janitorial bids in Arizona due this month."

One of the rows that comes back:

```json
{
  "title": "Districtwide Custodial Services",
  "agency": "Maricopa County Community Colleges",
  "state": "AZ",
  "dueDate": "2026-12-17T22:00:00",
  "source": "bonfire",
  "url": "https://maricopa.bonfirehub.com/opportunities/248049"
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/us-government-bids-rfps,talcoe/usaspending-awards,talcoe/sbir-awards
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--us-government-bids-rfps` | Open bids, RFPs and RFQs from SAM.gov, BidNet Direct, Bonfire and PlanetBids agency portals, and state and city procurement portals, filtered by keyword and state | $0.006 per bid |
| `talcoe--usaspending-awards` | Federal contract awards from USAspending.gov, filtered by NAICS code, agency, state and keyword | $0.005 per award |
| `talcoe--sbir-awards` | SBIR and STTR awards from SBIR.gov, filtered by agency, phase, state and keyword | $0.005 per award |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "Find janitorial bids in Arizona due this month."
- "Show open cybersecurity RFPs in Georgia, then the federal awards under NAICS 541512 in Georgia."
- "Which small businesses won Phase II SBIR awards from the Air Force in Ohio this year?"

## Source actors

- [Government Bids & RFPs Scraper](https://apify.com/talcoe/us-government-bids-rfps)
- [USAspending Federal Contract Awards Scraper](https://apify.com/talcoe/usaspending-awards)
- [SBIR/STTR Awards Scraper](https://apify.com/talcoe/sbir-awards)
