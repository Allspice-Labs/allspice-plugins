# NerdPress Guided Agent Connector

Connects bots to the publisher's own WordPress site through NerdPress's hosted
MCP, for site health checks and guided content changes.

## The endpoint is per site

NerdPress serves each site at its own URL:

```
https://support-mcp.nerdpress.net/mcp/<bare-domain>
```

`<bare-domain>` is the site's domain with no scheme and no trailing slash
(for example `butterandthyme.com`; a staging domain gets its own endpoint).
`example.com` in `mcp.json` is a placeholder: after installing, open
**Manage MCP servers** → this server and set the URL to the publisher's own
domain before connecting.

## Requirements and auth

- The site must run the NerdPress connector WordPress plugin
  (distributed by NerdPress at updates-connector.nerdpress.net).
- Connecting opens a NerdPress sign-in with the domain prefilled, then
  redirects to the site's own wp-admin **Authorize** page, where the owner
  picks what the connection may do. Read and some content edits default on;
  deletes, plugins, themes and updates default off.

## Writes card

This connector can change the publisher's site. Keep the workspace's approval
mode on Ask so every write tool call shows an approval card before it runs.
