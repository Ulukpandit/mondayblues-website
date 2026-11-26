# Monday Blues Website — mondayblues.net

Static, fast, SEO-first website for **Monday Blues-Digital marketing Services**, Mirzapur (UP). Built from the website brief as the single source of truth (NAP, services, testimonials, keywords).

## Pages

```
/                                        Home
/services/                               All services index
/digital-marketing-agency-mirzapur/      Main money page
/local-seo-mirzapur/                     Local SEO
/google-business-profile-optimisation-mirzapur/
/google-ads-mirzapur/                    Paid lead generation
/social-media-marketing-mirzapur/        Instagram & Facebook
/website-design-mirzapur/
/election-social-media-management-mirzapur/   Media vendor vertical
/about-kumar-neepu/
/contact/
```

## Included SEO setup

- Unique title tag, meta description and one H1 per page (service + Mirzapur)
- LocalBusiness JSON-LD (exact GBP NAP, geo, openingHours, priceRange, sameAs)
- Service schema on every service page, FAQPage schema (5 Qs each), Person schema on the about page
- sitemap.xml + robots.txt (submit in Google Search Console after deploy)
- Mobile-first, no frameworks, no render-blocking scripts (target LCP < 2.5s on 4G)
- Sticky click-to-call + WhatsApp bar on mobile

## ⚠️ Before launch — confirm these

1. **Phone number:** the site uses **088823 66931** everywhere (tap-to-call, WhatsApp, schema, footer). If the final number is 9519701143 instead, find-and-replace `918882366931` in all files. Use the SAME number on the Google Business Profile, Justdial and everywhere else.
2. **Instagram link in schema** currently points to https://www.instagram.com/uluk.pandit/ — replace with the official agency handle if that's different.
3. **Re-verify the review count/rating** (5.0 ★ / 21 reviews as of 25 Nov 2026) before publishing as a claim.
4. **Justdial hours** say "Open 24 Hrs" — change to Mon–Sat 10:00–18:00 to match the site and GBP.
5. aggregateRating is deliberately **omitted from schema** (Google ignores self-serving ratings for LocalBusiness); the 5.0 ★ badge on the page links to the live Google listing instead.

## Deploy (free, ~5 minutes)

### Netlify
1. app.netlify.com → **Add new site → Import an existing project → GitHub** → pick this repo
2. Build command: *(leave empty)* · Publish directory: *(leave empty / root)*
3. Site settings → Domain management → **Add custom domain** → `mondayblues.net` and `www.mondayblues.net` → follow the DNS instructions shown

### Vercel (alternative)
1. vercel.com → **Add New → Project** → import repo → Framework preset: **Other** → Deploy
2. Settings → Domains → add `mondayblues.net`

### DNS at your domain registrar
- Root `@` → A record to the IP Netlify/Vercel gives you (or ALIAS/ANAME)
- `www` → CNAME to the provided target
- HTTPS is automatic

## After deploy

1. Update the **Google Business Profile "Website" link** → `https://www.mondayblues.net` (currently points to astrologymarketing.in — wrong business)
2. Google Search Console → add property → submit `https://www.mondayblues.net/sitemap.xml`
3. Update the GBP WhatsApp chat link to the same number used on the site
4. Update Justdial hours + phone to match

## Editing content

Plain HTML/CSS — edit any `index.html` inside a page folder; shared styles in `/css/style.css`. No build step, no dependencies. Testimonials are verbatim Google reviews (first name + initial per the brief). Do not add fabricated stats, logos or reviews.
