# Calendly

Availability and bookings in Calendly, for brand calls and shoots.

Connects through Calendly's own hosted MCP server at `https://mcp.calendly.com/`.
Connecting opens Calendly's sign-in; the bots app registers itself with Calendly on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.calendly.com.

## Writes

This connector can change things in Calendly. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
