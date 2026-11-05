# Allspice Email

Lets a bot team draft the site's newsletter in the publisher's **own** email
platform, through the hosted Allspice Email MCP server
(`https://analytics-mcp.allspicelabs.com/email/mcp`): pick recipes from the site,
write the copy, lay it out in the site's brand, show the owner a preview in the
chat, and, once they approve it, save it as a **draft** in Kit, MailerLite or
Mailchimp for them to send.

## Drafts only

No tool on this server sends, schedules, deletes, or adds or removes subscribers,
and the service behind it has no way to. The publisher sends every email from their
own platform. Flodesk's API has no campaigns, so on Flodesk the bot can read lists
but cannot read past emails or create drafts. It hands the owner the email to paste
instead.

## Connecting

Install from the catalog (or **Integrations** → **+** → **From GitHub** with this
folder's URL), then sign in when prompted: the Allspice portal asks you to pick a
site and approve **email access**. That is a separate approval from the Allspice
Analytics connector, so an analytics connection never gets email tools. The site's
email platform must already be connected in the Allspice portal (Domain settings →
Email provider). This connector never asks for, stores or sees that platform's
key.

There is no API-key option: email access is only granted through that approval
screen, which records who approved it.

## What bots can do with it

- Read: the account and sender defaults, lists/tags/segments, recent campaigns with
  open and click stats, saved templates, the site's recipes, and what was promoted
  recently.
- Lay out an email (`render_email`) and attach its preview to the thread.
- Create or edit a **draft**, after the owner says yes. Those two tools are writes,
  so keep them behind approval cards (Ask mode).
