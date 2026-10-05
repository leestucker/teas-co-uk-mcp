# Installing teas.co.uk in Cline

teas.co.uk is a hosted remote MCP server, so there is nothing to download or build.

1. Open Cline's MCP settings (`cline_mcp_settings.json`).
2. Add this entry under `mcpServers`:

```json
{
  "mcpServers": {
    "teas.co.uk": {
      "type": "streamableHttp",
      "url": "https://teas.co.uk/mcp"
    }
  }
}
```

3. Save. Cline connects to `https://teas.co.uk/mcp` (Streamable HTTP).

No API key is needed. Searching, comparing products, recipes, the basket and checkout links work straight away.
Account tools (orders, tracking, repeat deliveries, reward points, returns) ask the customer to sign in to their
teas.co.uk account (OAuth 2.1) in clients that support it.

Try: "Find a strong breakfast tea, compare two options, add one to my basket and give me a checkout link."
