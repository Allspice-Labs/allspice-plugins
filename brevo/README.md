# Brevo

Contacts and email campaigns in Brevo.

Connects through Brevo's own hosted MCP server at `https://mcp.brevo.com/v1/brevo/mcp`.
Connecting opens Brevo's sign-in; the bots app registers itself with Brevo on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.brevo.com.

## Writes

This connector can change things in Brevo. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
