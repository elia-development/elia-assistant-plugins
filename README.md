# ELIA Assistant plugins

Plugins that connect Claude Code, Codex and ChatGPT to [ELIA Assistant](https://elia-assistant.com), so you can ask about your own account in plain language: what customers asked about this week, which interactions nobody has picked up, what one customer said recently, your Insights figures, or what your knowledge base could not answer.

The plugins contain no code and no credentials. Each one only names the ELIA Assistant MCP server, `https://elia-mcp.elia-assistant.com/mcp`. Tools come from that server, and every tool is read-only: nothing answers customers, claims interactions or changes data.

You sign in with your ELIA Assistant dashboard account (OAuth). The client opens the dashboard's consent page, you sign in and allow access, and from then on the plugin sees only that account's data. You need an ELIA Assistant account to use them.

| Folder | Client |
|---|---|
| `claude/elia-assistant` | Claude Code |
| `openai/elia-assistant` | Codex (CLI, IDE, app) and ChatGPT |

## Claude Code

```
/plugin marketplace add elia-development/elia-assistant-plugins
/plugin install elia-assistant@elia-assistant
```

Run `/mcp` and pick `elia-assistant` to sign in, or let the first tool call start it.

## Codex

```
codex plugin marketplace add elia-development/elia-assistant-plugins
codex plugin add elia-assistant@elia-assistant
```

Codex asks you to sign in when the plugin is installed.

## Other clients

Any MCP client that supports OAuth can use the server directly: add `https://elia-mcp.elia-assistant.com/mcp` as a remote (streamable HTTP) server. In claude.ai, use Settings > Connectors > Add custom connector.

## What data is sent

The client sends your questions' tool calls (search text, filters, dates, ids) to the MCP server, and the server returns your account's messages, interactions, customers, Insights figures and knowledge base content to the client. How ELIA Assistant handles that data is in the [privacy policy](https://elia-assistant.com/privacy-policy).

## Support

[elia-assistant.com/contact](https://elia-assistant.com/contact)
