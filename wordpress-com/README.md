# WordPress.com

Posts, pages and settings on a WordPress.com site.

Connects through WordPress.com's own hosted MCP server at `https://public-api.wordpress.com/wpcom/v2/mcp/v1`.
Connecting opens WordPress.com's sign-in; the bots app registers itself with WordPress.com on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to public-api.wordpress.com.

## Writes

This connector can change things in WordPress.com. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
