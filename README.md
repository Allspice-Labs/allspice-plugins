# Allspice plugins

The public plugin registry the Allspice bots app reads: each folder is an
Agent Plugins package (a `plugin.json` manifest plus an `mcp.json` server
config, and optional skills), and `marketplace.json` lists them for the in-app
catalog. This repository must stay public — the catalog and plugin installs
fetch it anonymously from GitHub — and must never contain credentials: keys
and per-site URLs are entered in the app after installing, where they are
stored encrypted.

- **allspice-analytics** — the hosted Allspice Analytics MCP (traffic, top
  posts, revenue). Fixed endpoint, OAuth 2.1 or a per-domain bearer key.
- **nerdpress-support** — NerdPress's Guided Agent Connector for the
  publisher's own WordPress site. Per-site endpoint; set the bare domain on
  the installed server. Its write tools must stay behind approval cards.
