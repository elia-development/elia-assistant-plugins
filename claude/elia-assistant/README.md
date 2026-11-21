# ELIA Assistant for Claude

Read your ELIA Assistant account from Claude: search customer messages across every channel, read one customer's recent conversation, list interactions handed over to your team, look up customers, get Insights figures for a period, and read the knowledge base your AI agents answer from.

This plugin contains no code and no credentials. It registers one remote MCP server, `https://elia-mcp.elia-assistant.com/mcp`, over HTTPS. You sign in with your ELIA Assistant dashboard account through OAuth, and the server then returns only that account's data. Every tool is read-only.

Install:

```
/plugin marketplace add elia-development/elia-assistant-plugins
/plugin install elia-assistant@elia-assistant
```

Privacy policy: https://elia-assistant.com/privacy-policy. Support: https://elia-assistant.com/contact.
