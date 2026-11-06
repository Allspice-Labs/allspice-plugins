# Wix

Pages, blog posts and store on a Wix site.

Connects through Wix's own hosted MCP server at `https://mcp.wix.com/mcp`.
Connecting opens Wix's sign-in; the bots app registers itself with Wix on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.wix.com.

## Writes

This connector can change things in Wix. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
