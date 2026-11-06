# Typeform

Reader surveys and their responses in Typeform.

Connects through Typeform's own hosted MCP server at `https://api.typeform.com/mcp`.
Connecting opens Typeform's sign-in; the bots app registers itself with Typeform on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to api.typeform.com.

## Writes

This connector can change things in Typeform. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
