# Rental Listings MCP server

Ask: "Find apartment buildings in Austin with units under $1,500."

One of the rows that comes back:

```json
{
  "buildingName": "Seabrook Square",
  "city": "Austin",
  "state": "TX",
  "minPrice": 1206,
  "maxPrice": 1932,
  "minBedrooms": 0,
  "maxBedrooms": 4,
  "minBathrooms": 1,
  "listingType": "building",
  "url": "https://www.zumper.com/apartment-buildings/p1503505/seabrook-square-mlk-austin-tx"
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/zumper-rentals
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--zumper-rentals` | Rental listings on Zumper by city, with rent, beds, baths, amenities and pet policy, filtered by property type, bedrooms, max rent and pets | $0.005 per listing |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "Find pet friendly two bedroom apartments in Austin under $1,800."
- "Compare one bedroom rents in Denver and Austin."
- "List Seattle buildings with in unit laundry under $2,500."

## Source actor

- [Zumper Rental Listings Scraper](https://apify.com/talcoe/zumper-rentals)
