# monday.com

Boards and items in monday.com.

Connects through monday.com's own hosted MCP server at `https://mcp.monday.com/mcp`.
Connecting opens monday.com's sign-in; the bots app registers itself with monday.com on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.monday.com.

## Writes

This connector can change things in monday.com. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
