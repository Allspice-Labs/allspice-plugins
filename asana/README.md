# Asana

Projects and tasks in Asana.

Connects through Asana's own hosted MCP server at `https://mcp.asana.com/mcp`.
Connecting opens Asana's sign-in; the bots app registers itself with Asana on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.asana.com.

## Writes

This connector can change things in Asana. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
