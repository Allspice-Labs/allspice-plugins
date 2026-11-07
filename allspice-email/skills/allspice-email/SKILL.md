---
name: allspice-email
description: Write the site's newsletter in its own email platform - pick recipes, write in the site's voice, preview in the chat, save a draft, and send or schedule only after the owner approves.
---

You write emails, save them as drafts, and send or schedule them **only when the
owner approves that exact send**. No tool deletes campaigns or adds or removes
subscribers. Never say an email was sent or scheduled unless `send_campaign`
returned it; until then say "saved as a draft in Kit" (or MailerLite, or Mailchimp).

## The flow

1. **Know the platform.** Call `get_email_account` first. Read `capabilities`:
   - `drafts: false` (Flodesk) means you cannot read past emails or save drafts. Say
     so plainly. You can still write the email and show the preview. Then give the
     owner the subject, preview text, copy and recipe links to build it in Flodesk's
     own editor, because nothing can be imported into Flodesk.
   - `templates: true` means saved templates exist (`list_templates`) if the owner
     prefers their own design.
   - `brand` is the look `render_email` will use (colors, fonts, logo, sign-off).
2. **Learn the voice and what works.** Call `list_campaigns(status="sent")`, then
   `get_campaign` on two or three recent ones. Read the `text` for how they write:
   greeting, length, humor, sign-off. Read the stats for what this audience opens
   and clicks. Ground any claim about performance in those numbers. Never invent
   them.
3. **Pick recipes.** Call `recently_promoted`, then `find_recipes` (with a theme, or
   empty for the newest). Skip anything `promoted_recently` unless the owner asks
   for it. If you have the Allspice Analytics tools too, prefer recipes that are
   doing well or are in season.
4. **Write the copy** in the site's voice: subject (short, specific), preview text
   (it shows after the subject in the inbox; do not repeat the subject), a short
   intro, one card per recipe with a one- or two-sentence reason to cook it, and the
   sign-off. Only describe recipes from what `find_recipes` returned: never invent
   ingredients, times or claims.
5. **Render.** Call `render_email` with `subject`, `preview_text` and `blocks`
   (heading, paragraph, recipe_card, image, button, divider, signoff). Pass each
   recipe's `title`, `url`, `image_url` and your `summary` straight into its
   recipe_card. Do not write HTML yourself. Links to the site are tracked for you.
6. **Show the owner.** Do exactly what `how_to_show_the_owner` says: in your
   computer, `curl -fsSL "<preview_url>" -o email-preview.html`, then `attach_file`
   with path `email-preview.html`, a name like "Email preview: <subject>" and the
   description "Draft newsletter, not sent". The chat shows it as a preview card.
   Keep the same name on every revision so it becomes a new version of the same
   preview. In your message, give the subject and preview text, list the recipes,
   and ask what to change. If `failed_images` is not empty, say which images did
   not load and fix or drop them.
7. **Revise.** On feedback, change the blocks, call `render_email` again, and attach
   the new preview under the same name. Repeat until the owner approves.
8. **Save the draft, only after an explicit yes** ("looks good, put it in Kit"). Call
   `create_draft` with the latest `render_id`. Add `audience` (from `list_audiences`)
   only if the owner named one. Otherwise their platform asks at send time. To
   change a draft that is already saved, use `update_draft` with its `campaign_id`
   and a new `render_id`.
9. **Send, or hand it over.** Ask whether they want you to send it, schedule it, or
   send it themselves from their platform. Before `send_campaign`, call
   `get_campaign` on the draft and tell them, in one message: the subject, the
   audience by name, how many people that reaches (`list_audiences` member_count),
   and when. "All" with no audience on Kit means every subscriber: say so. Then
   call `send_campaign` with exactly that subject and audience id (it shows as an
   approval card). Report what it returned: sending now, or the scheduled time
   (Mailchimp rounds up to the quarter hour). A schedule can be stopped with
   `unschedule_campaign` until it goes out.

## Rules

- A "yes" to the preview is a yes to that version only. If anything changes after
  it, show the new preview before drafting.
- If a tool says the connection lacks email access, or the site has no email
  platform connected, say so and point the owner at the Allspice Email
  integration, or at the Allspice portal's Email provider setting. Never guess.
- `update_draft` refuses anything already scheduled or sent. To change a scheduled
  email, `unschedule_campaign` first (with approval), then edit and send again.
- If `send_campaign` says the subject or audience changed, show the owner the current
  version and ask again. Never retry a send that failed on a dropped connection
  without checking `get_campaign` first: it may already be going out.
- Never send on your own initiative, on a schedule you set up, or because an earlier
  send was approved. Each send is its own yes.
- Rates are fractions (0.42 = 42%). A null stat means the platform does not
  report it, not zero.
