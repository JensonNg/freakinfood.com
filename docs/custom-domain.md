# Connect freakinfood.com (Tratto) to Blogger

The domain is registered at **Tratto**. Blogger serves the site; Tratto only holds the DNS records that point the domain at Google.

## 1. Start in Blogger

**Settings → Publishing → Custom domain** → enter `www.freakinfood.com` (use `www` — Blogger needs a subdomain).

Blogger then shows **two CNAME records**. Keep the page open.

## 2. Add the records at Tratto

Log in → open freakinfood.com → **DNS / DNS records / Zone editor** (wording varies).

| Type  | Name / Host | Value / Points to |
|-------|-------------|-------------------|
| CNAME | `www` | `ghs.google.com` |
| CNAME | the unique code Blogger shows (e.g. `abc123xyz`) | the unique `gv-….dv.googlehosted.com` value Blogger shows |
| A     | `@` (root) | `216.239.32.21` |
| A     | `@` | `216.239.34.21` |
| A     | `@` | `216.239.36.21` |
| A     | `@` | `216.239.38.21` |

- The second CNAME proves ownership and is unique to the blog — copy it exactly from Blogger.
- The four A records make bare `freakinfood.com` work.
- Delete any existing `www` or `@` records pointing elsewhere (e.g. a parking page) first.

## 3. Save in Blogger

Back on the Custom domain page, **Save**. DNS can take minutes to ~48 h. If Blogger errors, wait an hour and save again.

## 4. After it's live

In **Settings → Publishing / HTTPS**:

- **Redirect domain** → on (freakinfood.com → www.freakinfood.com)
- **HTTPS availability** → on (the certificate can take a few hours)
- **HTTPS redirect** → on

## 5. Google Search Console

Add a **Domain property** for `freakinfood.com` in Search Console. It asks for a **TXT record** — add it at Tratto the same way, then verify. Submit `https://www.freakinfood.com/sitemap.xml`.
