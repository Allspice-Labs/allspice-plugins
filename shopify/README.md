# Shopify

Products, orders and customers in the site's Shopify store (cookbooks, meal plans, merch).

Connects through Shopify's own hosted MCP server at `https://setup.shopify.com/mcp`.
Connecting opens Shopify's sign-in; the bots app registers itself with Shopify on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to setup.shopify.com.

## Writes

This connector can change things in Shopify. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
