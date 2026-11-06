# Canva

Pin graphics, social images and designs in Canva.

Connects through Canva's own hosted MCP server at `https://mcp.canva.com/mcp`.
Connecting opens Canva's sign-in; the bots app registers itself with Canva on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.canva.com.

## Writes

This connector can change things in Canva. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
