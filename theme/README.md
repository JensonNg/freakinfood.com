# Theme

The live theme is **Fooddy — FreakinFood edition**: Sora Templates' Fooddy 2.0 (free version), restyled to the FreakinFood design system.

## Put the live theme here

Commit Blogger's own backup — not a copy pasted from a browser or chat, which can silently change characters:

1. Blogger → **Theme** → **▾** (next to Customise) → **Backup** → **Download theme**.
2. Rename it `freakinfood-theme.xml` and add it to this folder
   (GitHub: **Add file → Upload files**).
3. Before every change to the live theme, download a fresh backup into `backups/` as `YYYY-MM-DD-freakinfood-theme.xml`.

## What the FreakinFood edition adds to the stock theme

- Design tokens as Blogger variables: `maincolor` rust `#9d4225`, `maindarkcolor` forest `#264224`, `greenmid` `#3d5a39`, `bodytext` `#434840`, `textdark` `#1b1c1c`, `sagemuted` `#c3c8bd`, surfaces `#ffffff` / `#f6f3f2` / `#eae8e7`.
- Newsreader / Be Vietnam Pro / Inter typography.
- Page-type classes on `<html>` (`ff-home`, `ff-about`, `ff-contact`, `ff-label`, `ff-item`) that show the homepage intro, author cards and contact form only where they belong.
- Per-post layouts from the post's label: `Post`, `Recipes` or `Reviews` adds `ff-article` plus `ff-type-*`.
- Recipe sheet (`.ff-rc-*`), review map, five-photo gallery and score rows (`.ff-map`, `.ff-gallery5`, `.ff-scores`).
- Sticky translucent nav, a hamburger panel on mobile in place of SelectNav, and the Contact link styled as a call to action.
- Reading time in the byline, and stars generated from review scores.

## Known leftovers from the stock template

Worth cleaning up eventually; none of them block anything:

- An obfuscated vendor script near the end ("Theme Functions JS"). In free Sora templates this usually enforces the footer credit link. It hasn't been decoded or reviewed.
- Instafeed (uses Instagram's retired v1 API), the Facebook SDK on every page, jQuery 1.11.0.
- Footer **Tags** widget still lists the demo labels (Blueberry, Curry, Mexican…); footer social links all point to `#`.
- A `.ff-recipe` "recipe list fix" block that targets an older recipe markup no longer used by `.ff-rc-sheet`.
