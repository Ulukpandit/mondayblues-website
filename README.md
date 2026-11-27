# Monday Blues Website — mondayblues.net

Static, fast, SEO-first website for **Monday Blues-Digital marketing Services**, Mirzapur (UP). Built from the website brief as the single source of truth (compiled 25 Nov 2026 from the Google Business Profile, Justdial and existing domains).

## Pages

```
/                                            Homepage
/services/                                   Services index (core + also-offered)
/digital-marketing-agency-mirzapur/          Main money page
/local-seo-mirzapur/                         Local SEO
/google-business-profile-optimisation-mirzapur/  GBP optimisation
/google-ads-mirzapur/                        Google Ads / paid leads
/social-media-marketing-mirzapur/            Instagram & Facebook
/website-design-mirzapur/                    Website design & development
/election-social-media-management-mirzapur/  Election vertical (media vendor)
/about-kumar-neepu/                          Founder page (Person schema)
/contact/                                    Contact + map
```

Plus: `css/style.css`, `js/main.js`, `sitemap.xml`, `robots.txt`, `404.html`. Plain HTML — no build step, no frameworks, mobile-first, sticky Call + WhatsApp bar on mobile.

## ⚠️ Before launch — confirm these

1. **Phone number:** the site uses **088823 66931** everywhere (call links, WhatsApp `wa.me/918882366931`, schema). If the final agreed number is 9519701143 instead, search-and-replace `918882366931` → `919519701143` across all files.
2. **Instagram:** schema `sameAs` points to `https://www.instagram.com/uluk.pandit/` — replace with the official agency handle if different.
3. **Justdial:** hours there say "Open 24 Hrs" — change to Mon–Sat 10:00–18:00 to match Google and the site.
4. **Review claims:** re-verify "5.0 ★ from 21 reviews" on the day you publish — the number will move.
5. **Old template content:** do not reuse anything from the current live mondayblues.net (Lorem Ipsum logos, bKash/Ahmed Karim testimonials, "120+ Projects"). This repo contains none of it.

## Deploy (5 minutes)

### Netlify (recommended)
1. app.netlify.com → **Add new site → Import an existing project → GitHub** → pick `mondayblues-website`.
2. Build command: *(leave empty)* · Publish directory: `.`
3. Site settings → Domain management → **Add custom domain** → `mondayblues.net` (and `www`) → follow the DNS instructions shown (A/CNAME records at your domain registrar).

### Vercel
- vercel.com → Add New Project → import the repo → Framework preset: **Other** → Deploy → add `mondayblues.net` in Domains.

### Cloudflare Pages
- Connect repo → build command: none, output dir: `/` → add custom domain.

## After deploy

1. **Google Business Profile:** change the profile's Website link from `astrologymarketing.in` → `https://www.mondayblues.net`.
2. **Google Search Console:** add the property → submit `https://www.mondayblues.net/sitemap.xml`.
3. **GBP WhatsApp chat link:** point it at the same number used on the site (one number everywhere).
4. Optional: add a real case study (e.g., Aqua Fair RO System) **only with written client permission**.

## Editing

Edit any `index.html` in its folder; shared design lives in `css/style.css`. No build tools required.

## SEO notes

- Unique title, meta description and single H1 per page (service + city).
- JSON-LD: LocalBusiness (exact NAP + geo + opening hours) on every page; Service + FAQPage on service pages; Person for Kumar Neepu.
- `aggregateRating` is intentionally **omitted** from schema — Google ignores self-serving ratings on LocalBusiness markup. The 5.0 ★ / 21 reviews is shown as visible text linking to the Google listing instead.
- Sitemap lists all 11 URLs at `https://www.mondayblues.net` — update the hostname if you deploy on a different domain first.
