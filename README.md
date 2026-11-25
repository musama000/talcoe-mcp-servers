# Talcoe MCP servers

Remote MCP servers that give AI agents US public data: government bids, council agendas and business registries. Each server is a set of [Talcoe actors on Apify](https://apify.com/talcoe) loaded into Apify's hosted MCP server, so there is nothing to install or run.

| Server | Ask it | Tools inside |
|---|---|---|
| [US Government Bids](servers/us-government-bids) | "Find janitorial bids in Arizona due this month." | Open bids and RFPs, federal contract awards, SBIR and STTR awards |
| [Public Meeting Agendas](servers/public-meeting-agendas) | "What contracts are on Denver's committee agendas this week?" | City council, county board and school board agenda items |
| [US Business Entities](servers/us-business-entities) | "List plumbing LLCs formed in Colorado this month." | Business registry records from CO, NY, OR and CT |

## Connect

Each server is one URL, listed on its page. Send your Apify API token in the `Authorization` header. You can create a token at [console.apify.com/settings/integrations](https://console.apify.com/settings/integrations).

To add the bids server to Claude Code, run this command with your token in place of YOUR_APIFY_TOKEN.

```bash
claude mcp add --transport http us-government-bids "https://mcp.apify.com/?tools=talcoe/us-government-bids-rfps,talcoe/usaspending-awards,talcoe/sbir-awards" --header "Authorization: Bearer YOUR_APIFY_TOKEN"
```

Cursor reads `~/.cursor/mcp.json`, and other clients that take a URL plus headers use the same shape.

```json
{
  "mcpServers": {
    "us-government-bids": {
      "url": "https://mcp.apify.com/?tools=talcoe/us-government-bids-rfps,talcoe/usaspending-awards,talcoe/sbir-awards",
      "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" }
    }
  }
}
```

VS Code reads `.vscode/mcp.json` and can prompt for the token.

```json
{
  "inputs": [
    { "id": "apify_token", "type": "promptString", "description": "Apify API token", "password": true }
  ],
  "servers": {
    "us-government-bids": {
      "type": "http",
      "url": "https://mcp.apify.com/?tools=talcoe/us-government-bids-rfps,talcoe/usaspending-awards,talcoe/sbir-awards",
      "headers": { "Authorization": "Bearer ${input:apify_token}" }
    }
  }
}
```

Clients that support MCP sign in (OAuth) can connect with the URL alone and log in to Apify in the browser.

## Pricing

Results cost 0.4 to 1.5 cents each, billed to your Apify account at the actor's Store price, and each run carries a small start charge. The server pages list every price. An agent without an Apify account can buy a prepaid token with USDC over x402, with Skyfire or with a US card at [agi.apify.com](https://agi.apify.com).

## Registry

The `server.json` files in `servers/` are the listings published to the [official MCP Registry](https://registry.modelcontextprotocol.io) under `io.github.musama000/*`.

Open an issue if a tool breaks or you need a source we don't cover yet.
