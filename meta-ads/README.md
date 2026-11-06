# Meta Ads

Facebook and Instagram ad campaigns and their results.

Connects through Meta Ads's own hosted MCP server at `https://mcp.facebook.com/ads`.
Connecting opens Meta Ads's sign-in; the bots app registers itself with Meta Ads on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.facebook.com.

## Writes

This connector can change things in Meta Ads. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
