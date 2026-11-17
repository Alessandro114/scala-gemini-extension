# S.C.A.L.A. AI — Gemini CLI extension

Ask Gemini about your S.C.A.L.A. AI data: pipeline, cash flow, SARA alerts, workflow errors.

- **Read-only.** 14 tools; nothing is created, changed, deleted or sent, and no money moves.
- **Needs a S.C.A.L.A. account** on Growth, Scale or Enterprise, or the 14-day Growth trial (no card): https://app.get-scala.com
- **Limits:** 120 requests/minute/user; access tokens last 1 hour and renew for up to 30 days.
- Support: support@get-scala.com · Privacy: https://get-scala.com/en/privacy · Connector docs: https://github.com/Alessandro114/scala-mcp-server/blob/main/docs/claude-connector.md

> **Status: early release.** The connector works with Claude today. This Gemini CLI extension has not yet been verified end to end with every Gemini CLI version. If sign-in fails, write to support@get-scala.com with the exact error.

## Install

```bash
gemini extensions install https://github.com/Alessandro114/scala-gemini-extension
```

## Manual setup (without the extension)

```bash
gemini mcp add --transport http scala https://mcp.get-scala.com/mcp
```
or in `~/.gemini/settings.json`:
```json
{ "mcpServers": { "scala": { "httpUrl": "https://mcp.get-scala.com/mcp" } } }
```
Then run `/mcp auth scala` inside Gemini CLI. A browser opens on the same machine for sign-in with your S.C.A.L.A. account; click **Allow**. OAuth does not work on headless machines or plain SSH sessions.

Antigravity CLI uses `serverUrl` instead of `httpUrl` and its own config file (see Google's Antigravity MCP docs).

## License

MIT
