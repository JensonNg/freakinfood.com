# freakinfood.com

Recipes, food curiosities and café & restaurant reviews from Ema & Son: Vietnamese and Italian cooking out of a Nordic kitchen.

The site runs on **Blogger** at **www.freakinfood.com** (domain registered at Tratto). This repo holds the theme, the post snippets, brand assets and setup docs. Blogger doesn't read from GitHub, so changes are copied in by hand (see [docs/deploy-to-blogger.md](docs/deploy-to-blogger.md)).

## What's here

```
theme/
  freakinfood-theme.xml   FreakinFood theme v2 for Blogger
  backups/                Dated downloads of the live theme, one before every change
  README.md               What the theme does, labels it expects
snippets/
  recipe-card.html        Recipe sheet (.ff-rc-*) + schema.org Recipe JSON-LD for posts
assets/                   Logos, favicon, social images
docs/
  deploy-to-blogger.md    Updating the theme safely
  custom-domain.md        Pointing freakinfood.com (Tratto) at Blogger
  seo-checklist.md        Search, Pinterest, Instagram and Flipboard
  social-kit.md           Instagram / Pinterest / Flipboard templates
```

## Site structure

| Section | URL | Label |
|---|---|---|
| Home | `/` | — |
| Blog (all posts) | `/search` | — |
| Posts | `/search/label/Post` | `Post` |
| Recipes | `/search/label/Recipes` | `Recipes` |
| Reviews | `/search/label/Reviews` | `Reviews` |
| About | `/p/about-us.html` | — |
| Contact | `/p/contact-us.html` | — |

## Design system

- **Colours:** paper `#fbf9f8`, forest `#264224`, green mid `#3d5a39`, rust `#9d4225` (the one accent), body `#434840`, heading text `#1b1c1c`, sage `#c3c8bd`, surfaces `#ffffff` / `#f6f3f2` / `#eae8e7`.
- **Type:** Newsreader ExtraLight italic for headings, Be Vietnam Pro for body, Inter uppercase for labels (Google Fonts).
- **Pattern:** rust eyebrow → large green italic title → one muted intro line.
