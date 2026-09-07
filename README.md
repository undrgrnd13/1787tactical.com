# 1787tactical.com

Phase 1 static marketing site for **1787 TACTICAL, LLC.** — Type 07 FFL, Loxahatchee, FL.

**In-person sales only. By appointment only — call/text first. No walk-ins. No cart.**

## Pages

| File | Purpose |
|------|---------|
| `index.html` | Home — brand, tagline, appointment CTA, featured builds |
| `builds.html` | All sample product cards (AR-15s + ProMag) with call-to-buy CTAs |
| `about.html` | FFL trust, transfer fees, payments, NFA, 4473/FDLE policies |
| `contact.html` | NAP, phone, email mailto, appointment scheduling windows |
| `sitemap.xml` / `robots.txt` | SEO crawl files |
| `images/` | Compressed product JPEGs (local; see image note) |

## Contact (NAP)

- **Legal:** 1787 TACTICAL, LLC.
- **Address:** 16971 W Hialeah Dr, Loxahatchee, FL 33470
- **Phone:** 561-985-6696 (call or text)
- **Email:** 1787@1787TACTICAL.COM

## Appointment policy

**By appointment only.** Hours below are when appointments can be **scheduled** — not walk-in hours:

- Mon–Fri 12pm–7pm
- Sat 10am–5pm
- Sun 12pm–4pm

## FFL display policy

Public site shows **Type 07 FFL** / licensed manufacturer only. **Do not publish the full FFL license number.** Full number is provided to transferring FFLs on request. License expires Nov 1, 2026 (stated as current without posting the number).

## Redirects (configure on Porkbun / host)

| Old path | New target |
|----------|------------|
| `/about` | `/about.html` |
| `/contact` | `/contact.html` |
| `/c/cart` | `/` (drop cart) |
| `/builds` | `/builds.html` (optional pretty URL) |

Optional: `/ffl` → `/about.html`.

## Dropped from Articulation

- Cart chrome and `/c/cart`
- $0 “Product Name” placeholder ammo card
- Dead “Get Started” / “More…” menus
- Articulation contact form (replaced with tel + mailto)

## Products (display only)

| Name | Price |
|------|-------|
| AR-15 Sample Build A | $400 |
| AR-15 Sample Build B | $425 |
| AR-15 Sample Build C | $400 |
| AR-15 Sample Build D | $415 |
| ProMag 30 Round | $12 |
| ProMag 42 Round | $15 |

Prices are indicative — call to confirm. No add-to-cart.

## Image assets note

Product photos were downloaded from the Articulation CDN and compressed into `images/*.jpg`. **GitHub MCP `push_files` corrupts binary blobs**, so HTML currently references the Articulation CDN URLs for reliable preview. Follow-up: PAT/`gh` git push of `images/` then switch `src` to relative paths before canceling Articulation.

CDN base: `https://a1694c05-02c2-45b0-801e-8c7aad8cbc80.assets.articulation.website/storage/329/a1694c05-02c2-45b0-801e-8c7aad8cbc80/`

## Deploy

Public GitHub repo → Porkbun Static Hosting. Prefer PRs for content changes. **Do not merge** until Paul reviews.

## Out of scope (v1)

Payments, GunBroker, shipping firearms to individuals, cart/checkout.
