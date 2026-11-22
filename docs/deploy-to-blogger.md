# Updating the theme on Blogger

Blogger doesn't deploy from GitHub. `theme/freakinfood-theme.xml` is the source of truth; changes are copied into Blogger by hand.

## Every change

1. **Back up the live theme:** Theme → ▾ → **Backup** → Download theme. Commit it to `theme/backups/YYYY-MM-DD-freakinfood-theme.xml`.
2. Edit `theme/freakinfood-theme.xml` in this repo and commit.
3. Blogger → Theme → ▾ → **Edit HTML** → select all → paste the new file → **Save**.
   If Blogger reports an XML error it gives a line number; fix it here and paste again.
4. Check on desktop and phone:
   - homepage (intro, latest-posts grid, author cards)
   - `/search` and a label page (pills switch sections)
   - one post each labelled **Post**, **Recipes** and **Reviews**
   - `/p/about-us.html` and `/p/contact-us.html` (contact form shows only here)
5. If something breaks: Theme → ▾ → **Restore** → upload the backup from step 1.

## How the site is wired

- **Labels drive layouts.** `Post`, `Recipes` and `Reviews` switch a post to its layout; label pages get their intro line from the theme. Use exactly these spellings.
- **Menu:** Layout → Main Menu. A leading `_` makes an item a sub-item (`_Recipes` sits under Blog). Any link containing `contact` gets the green button style.
- **Editable blocks (Layout tab):** Homepage intro, Author cards, Contact page form, Follow Us (sidebar), footer about text.

## Changing colours

Theme → Customise → Advanced lists the colour variables (rust, forest green, green mid, body text…). Quick tweaks there are fine, but download the theme afterwards and commit it so the repo matches.
