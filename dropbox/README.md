# Dropbox

Photos and files in Dropbox, such as recipe shoots.

Connects through Dropbox's own hosted MCP server at `https://mcp.dropbox.com/mcp`.
Connecting opens Dropbox's sign-in; the bots app registers itself with Dropbox on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.dropbox.com.

## Writes

This connector can change things in Dropbox. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
