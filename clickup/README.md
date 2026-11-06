# ClickUp

Tasks, docs and lists in ClickUp.

Connects through ClickUp's own hosted MCP server at `https://mcp.clickup.com/mcp`.
Connecting opens ClickUp's sign-in; the bots app registers itself with ClickUp on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.clickup.com.

## Writes

This connector can change things in ClickUp. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
