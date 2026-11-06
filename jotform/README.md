# Jotform

Forms and submissions in Jotform.

Connects through Jotform's own hosted MCP server at `https://mcp.jotform.com`.
Connecting opens Jotform's sign-in; the bots app registers itself with Jotform on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.jotform.com.

## Writes

This connector can change things in Jotform. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
