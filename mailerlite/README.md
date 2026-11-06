# MailerLite

Newsletter subscribers, groups, campaigns and automations in MailerLite.

Connects through MailerLite's own hosted MCP server at `https://mcp.mailerlite.com/mcp`.
Connecting opens MailerLite's sign-in; the bots app registers itself with MailerLite on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.mailerlite.com.

## Writes

This connector can change things in MailerLite. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
