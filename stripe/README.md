# Stripe

Payments, customers and products in Stripe, such as cookbook or meal plan sales.

Connects through Stripe's own hosted MCP server at `https://mcp.stripe.com`.
Connecting opens Stripe's sign-in; the bots app registers itself with Stripe on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.stripe.com.

## Writes

This connector can change things in Stripe. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
