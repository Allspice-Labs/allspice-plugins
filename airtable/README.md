# Airtable

Bases and records in Airtable, such as a content plan or brand deal tracker.

Connects through Airtable's own hosted MCP server at `https://mcp.airtable.com/mcp`.
Connecting opens Airtable's sign-in; the bots app registers itself with Airtable on the first
connection, so there are no keys to paste. Tokens stay encrypted in the bots app and calls go
straight to mcp.airtable.com.

## Writes

This connector can change things in Airtable. Keep the workspace's approval mode on Ask so
every write shows an approval card before it runs.
