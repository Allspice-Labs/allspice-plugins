# QuickBooks

Income, expenses and invoices in QuickBooks Online.

Connects through QuickBooks's own hosted MCP server at `https://mcp-e2e.quickbooks.intuit.com/mcp`.
Connecting opens QuickBooks's sign-in; the bots app registers itself with QuickBooks on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp-e2e.quickbooks.intuit.com.

## Writes

This connector can change things in QuickBooks. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
