# Notion

Pages and databases in Notion, such as an editorial calendar or recipe notes.

Connects through Notion's own hosted MCP server at `https://mcp.notion.com/mcp`.
Connecting opens Notion's sign-in; the bots app registers itself with Notion on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.notion.com.

## Writes

This connector can change things in Notion. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
