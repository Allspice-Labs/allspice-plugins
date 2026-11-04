# Allspice Analytics

Connects a bot team to the site's live analytics through the hosted Allspice
Analytics MCP server (`https://analytics-mcp.allspicelabs.com/mcp`): top posts
over a date range, traffic trends, and revenue summaries.

## Connecting

Install from the catalog (or **Integrations** → **+** → **From GitHub** with
this folder's URL), then sign in when prompted — the server speaks OAuth 2.1
with discovery, so the connect flow is the server's own sign-in.

For a key instead of OAuth (a per-domain `asx_live_…` key issued by Allspice):
after installing, open **Manage MCP servers** → this server → **Advanced** and
set the header `Authorization: Bearer asx_live_…`. Keys are stored encrypted
and never shown to the model. Never commit a key to this repository.

## What bots can do with it

All analytics tools are read-only. Writes do not exist on this server; anything
a bot wants to change elsewhere still cards through the usual approval flow.
