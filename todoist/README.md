# Todoist

Tasks and projects in Todoist.

Connects through Todoist's own hosted MCP server at `https://ai.todoist.net/mcp`.
Connecting opens Todoist's sign-in; the bots app registers itself with Todoist on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to ai.todoist.net.

## Writes

This connector can change things in Todoist. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
