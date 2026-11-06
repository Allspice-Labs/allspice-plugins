# Buffer

Draft and schedule social posts across the channels connected to Buffer.

Connects through Buffer's own hosted MCP server at `https://mcp.buffer.com/mcp`.
Connecting opens Buffer's sign-in; the bots app registers itself with Buffer on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.buffer.com.

## Writes

This connector can change things in Buffer. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
