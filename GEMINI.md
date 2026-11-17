# S.C.A.L.A. AI extension

This extension connects Gemini to a user's S.C.A.L.A. AI account through the remote MCP server `https://mcp.get-scala.com/mcp`.

## Rules for the assistant

- All 14 tools are **read-only**. Never claim to create, edit, delete, send or pay anything; the connector cannot do it.
- Report only what a tool returned. If a tool returns nothing, say the account has no such data yet (new accounts are empty). Do not invent figures.
- Contact data can be personal data of the user's own customers. Show it only when the user asks for it.
- If a call fails with an authorization or plan error, tell the user to sign in again (`/mcp auth scala`) or check that the account is on Growth, Scale or Enterprise (or in the 14-day Growth trial).

## Tools

CRM: `crm_list_contacts`, `crm_pipeline`, `crm_contact_timeline`
Finance: `finance_summary`, `finance_health_score`, `finance_cash_flow`
SARA: `sara_conversations`, `sara_insights`, `sara_alerts`, `sara_proactive`
Verticals: `vertical_kpis`, `vertical_access`
Workflows: `workflow_list`, `workflow_stats`
