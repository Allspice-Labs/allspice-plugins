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

## Vendor connectors

Each of these points at the vendor's own hosted MCP server. The bots app registers
itself with the vendor on first connect (OAuth dynamic client registration, or a
client metadata document for Shopify), so nothing here holds a key. Write-capable
ones carry a Writes note in their README: keep approvals on Ask.

- **mailerlite**: MailerLite. Newsletter subscribers, groups, campaigns and automations in MailerLite.
- **beehiiv**: beehiiv. Newsletter posts, subscribers and tags in beehiiv.
- **klaviyo**: Klaviyo. Email profiles, segments, campaigns and flows in Klaviyo.
- **brevo**: Brevo. Contacts and email campaigns in Brevo.
- **semrush**: Semrush. Keyword research, rankings, backlinks and competitor traffic from Semrush.
- **ahrefs**: Ahrefs. Keywords, backlinks, rankings and site health from Ahrefs.
- **similarweb**: Similarweb. Traffic estimates and audience comparisons for any site.
- **profound**: Profound. How often AI answers mention and cite the site, from Profound.
- **buffer**: Buffer. Draft and schedule social posts across the channels connected to Buffer.
- **meta-ads**: Meta Ads. Facebook and Instagram ad campaigns and their results.
- **tiktok-for-business**: TikTok for Business. TikTok ad campaigns, audiences and reports.
- **shopify**: Shopify. Products, orders and customers in the site's Shopify store (cookbooks, meal plans, merch).
- **square**: Square. Payments, orders, catalog and invoices in Square.
- **quickbooks**: QuickBooks. Income, expenses and invoices in QuickBooks Online.
- **hunter**: Hunter. Find and verify contact emails for brand partnership pitches.
- **typeform**: Typeform. Reader surveys and their responses in Typeform.
- **jotform**: Jotform. Forms and submissions in Jotform.
- **calendly**: Calendly. Availability and bookings in Calendly, for brand calls and shoots.
- **todoist**: Todoist. Tasks and projects in Todoist.
- **trello**: Trello. Boards and cards in Trello, such as an editorial calendar.
- **fathom**: Fathom. Meeting recordings, summaries and action items from Fathom.
- **gamma**: Gamma. Make presentations and documents in Gamma, such as a media kit.
- **occasio**: Occasio. Content intelligence for the site's posts from Occasio, built on its Google Analytics and Search Console data.

Vendor logos are their owners' trademarks, shown to identify the service. They come
from cursor/plugins (MIT licensed).
