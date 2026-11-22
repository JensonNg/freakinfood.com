# Theme

`freakinfood-theme.xml` is **FreakinFood theme v2**: written from scratch from the FreakinFood design system and the homepage redesign. It replaces the Sora "Fooddy" base. It has no jQuery, no Font Awesome and no third-party scripts, and needs no credit link.

## What's in it

| Area | How it works |
|---|---|
| Header | One 66px sticky bar: logo (Layout › Logo), menu (Layout › Main Menu), search. Hamburger panel under 880px. Any menu link containing `contact` becomes the green button. |
| Homepage hero | Left: **Homepage intro** HTML gadget (eyebrow, H1, intro, buttons). Right: **Homepage featured post** gadget, the post you pick in Layout, with the "Today's pick" card. |
| Today's Highlights | The 3 newest posts labelled **Highlight**, loaded from the blog feed. The section hides itself if no post has that label. |
| Latest from the Blog | The normal post list, as a 4-up card grid. Count = Settings › Posts › "Number of posts on main page" (4 or 8). |
| Explore | Four tiles linking to the Recipes, Drinks, Stories and Reviews labels. |
| Who We Are | **Who we are** HTML gadget: your text, both of you, "About our pictures". Homepage only. |
| Newsletter | **Newsletter** HTML gadget on every page. Its form needs your newsletter service's form action. |
| Label / search pages | Header with section intro and pills (All · Recipes · Drinks · Stories · Reviews), 3-up card grid, pager. |
| Posts and pages | One centred column, section label, H1, byline · date · read time; tags, share links (Pinterest, Facebook, WhatsApp, Email), newer/older, Blogger comments. |
| Post blocks | Everything from v1 still works inside posts: `.ff-standfirst`, `.ff-lead`, `.ff-pullquote`, `p.ff-dropcap`, the recipe sheet `.ff-rc-*` (`snippets/recipe-card.html`), review `.ff-map`, `.ff-gallery5`, `.ff-scores` (numbers become stars). |
| Contact page | **Contact page form** gadget, shown only on `/p/contact-us.html`. |

## Labels the theme expects

`Recipes`, `Drinks`, `Stories`, `Reviews` for sections, plus `Highlight` to feature a post on the homepage (hidden from the card label line).
Old posts labelled `Post` or `Food Talk` should be relabelled `Stories`.

## Colours

Theme › Customise › Advanced still lists the same colour variables as before (Rust, Forest Green, Primary Mid, Body Text…).

## Backups

Before every change to the live theme, download it (Theme › ▾ › Backup) into `backups/` as `YYYY-MM-DD-freakinfood-theme.xml`.
