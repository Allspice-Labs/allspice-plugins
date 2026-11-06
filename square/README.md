# Square

Payments, orders, catalog and invoices in Square.

Connects through Square's own hosted MCP server at `https://mcp.squareup.com/mcp`.
Connecting opens Square's sign-in; the bots app registers itself with Square on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.squareup.com.

## Writes

This connector can change things in Square. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
