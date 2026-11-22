# Testing and installing theme v2

Blogger doesn't deploy from GitHub: `theme/freakinfood-theme.xml` is copied in by hand.

## 1. Test on a spare blog first

1. In Blogger, **New blog** → e.g. "FreakinFood test". Keep it private (Settings › Permissions › Reader access: Private).
2. Copy a few real posts in, with images. Give them the labels **Recipes**, **Drinks**, **Stories**, **Reviews**, and add **Highlight** to three of them.
3. Create two pages: **About us** (URL `/p/about-us.html`) and **Contact us** (`/p/contact-us.html`).
4. **Theme › ▾ › Restore › Upload** `freakinfood-theme.xml`.
   If Blogger shows an error, copy the message (it has a line number) and send it over.

## 2. Set up the gadgets (Layout tab)

| Gadget | What to do |
|---|---|
| Logo | Already points to your logo image. To change it: upload a new image, "Instead of title and description". |
| Main Menu | Check the links. `/search/label/…` links go to label pages. |
| Homepage intro | Edit the text if you like; keep the `class` names. |
| Homepage featured post | Untick "Use most recent post" and pick the post for the hero. Its first image is the hero photo; a tall (portrait) image works best. |
| Who we are | Edit text and photos. |
| Newsletter | Replace `action="#"` with your newsletter service's form action (see below). |
| Contact page form | Nothing to do; it appears on the Contact page only. |

Settings › Posts › **Number of posts on main page**: 4 (one row) or 8 (two rows).

## 3. Check

- Homepage on desktop and phone: hero, Today's Highlights, Latest, Explore, Who we are, Newsletter, footer.
- A label page (`/search/label/Recipes`): heading, pills, grid, older posts link.
- A post with the recipe sheet, a review with map/gallery/scores, comments on a post.
- `/p/contact-us.html`: the form shows and sends.
- The menu button and search on a phone.

## 4. Go live

1. Back up the live theme (Theme › ▾ › Backup) and commit it to `theme/backups/`.
2. Restore the new theme on the live blog, then redo step 2 there.
3. Relabel old posts: `Post` / `Food Talk` → `Stories`; add `Drinks` where it fits; tag three posts `Highlight`.
4. Rebuild the old hand-made homepage links: the theme now fills the homepage by itself, so the old homepage **page** (with links to the Blogger editor) can be deleted or turned into a draft.

If anything breaks: Theme › ▾ › Restore → upload the backup from step 4.1.

## Newsletter

Blogger's old "Follow by Email" stopped sending emails in 2021. Pick a service (MailerLite and Brevo have free tiers), create a signup form, and copy its **form action URL** and **email field name** into the Newsletter gadget (`action="…"` and `name="…"`).
