# Allspice Email

Lets a bot team write the site's newsletter in the publisher's **own** email
platform, through the hosted Allspice Email MCP server
(`https://email-mcp.allspicelabs.com/mcp`): pick recipes from the site, write the
copy, lay it out in the site's brand, show the owner a preview in the chat, save it
as a **draft** in Kit, MailerLite or Mailchimp, and send or schedule it once the
owner approves.

## Sending

Every send, schedule and unschedule waits for an approval card in the chat. The send
carries the subject and audience the owner approved, and is refused if the draft
changed after that. A scheduled email can be unscheduled until it goes out. No tool
deletes campaigns or adds or removes subscribers. Flodesk's API has no campaigns, so
on Flodesk the bot can read lists but cannot read past emails, draft or send. It
still writes and previews the email, then hands the owner the copy to build it in
Flodesk's editor.

## Connecting

In the Allspice bots, turn on **Settings → Allspice connections → Let the team
draft emails**. It connects with your Allspice sign-in and asks for **email access**
for your site. That is a separate approval from the Allspice
Analytics connector, so an analytics connection never gets email tools. The site's
email platform must already be connected in the Allspice portal (Domain settings →
Email provider). This connector never asks for, stores or sees that platform's
key.

There is no API-key option: email access is only granted through that switch, which
records who approved it.

## What bots can do with it

- Read: the account and sender defaults, lists/tags/segments, recent campaigns with
  open and click stats, saved templates, the site's recipes, and what was promoted
  recently.
- Lay out an email (`render_email`) and attach its preview to the thread.
- Create or edit a **draft**, after the owner says yes.
- Send it now or schedule it (`send_campaign`), or stop a schedule
  (`unschedule_campaign`). Every one of these writes waits for an approval card.
