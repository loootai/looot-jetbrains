# looot for JetBrains IDEs

looot gives an AI agent one key and one prepaid balance for 2,500+ data API endpoints from 90+ providers: work emails, phone numbers, company and people search, Google results, web pages, news, LinkedIn profiles, local businesses. The agent sees the price before it runs, and a failed call costs nothing. Top up from $5.

JetBrains has no plugin API for registering an external MCP server, and no marketplace listing for one. The plugin extension points in the IDE expose IDE tools as an MCP server, which is the opposite direction. So there is no looot plugin. Setup is a JSON paste, and it works in every IDE that has AI Assistant 2026.1 or newer (IntelliJ IDEA, PyCharm, WebStorm, GoLand, Rider and the rest).

## AI Assistant

1. Open Settings | Tools | AI Assistant | Model Context Protocol (MCP).
2. Click Add.
3. Choose the HTTP (Streamable HTTP) transport and paste:

```json
{
  "mcpServers": {
    "looot": {
      "url": "https://api.looot.ai/mcp"
    }
  }
}
```

4. Click OK, then Apply. The looot tools appear in the AI Assistant chat.

If you already added looot to Claude Desktop, use "Import from Claude" on the same page.

## Junie

Open Settings | Tools | Junie | MCP Settings and add the same JSON.

## Sign-in

looot's server uses OAuth in the browser. The JetBrains docs do not say whether remote servers support OAuth, and we have not tested this in a JetBrains IDE yet. If the sign-in window does not open, contact https://looot.ai/contact.

[looot.ai](https://looot.ai) | [Docs](https://docs.looot.ai) | [Support](https://looot.ai/contact)
