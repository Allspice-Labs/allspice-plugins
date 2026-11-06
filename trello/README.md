# Trello

Boards and cards in Trello, such as an editorial calendar.

Connects through Trello's own hosted MCP server at `https://mcp.trello.com/v1`.
Connecting opens Trello's sign-in; the bots app registers itself with Trello on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.trello.com.

## Writes

This connector can change things in Trello. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
