# Klaviyo

Email profiles, segments, campaigns and flows in Klaviyo.

Connects through Klaviyo's own hosted MCP server at `https://mcp.klaviyo.com/mcp`.
Connecting opens Klaviyo's sign-in; the bots app registers itself with Klaviyo on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.klaviyo.com.

## Writes

This connector can change things in Klaviyo. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
