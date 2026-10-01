# Hearthside Printables — Free SEO Static Site

A pure static HTML + CSS website (no build step, no JavaScript, no external dependencies)
that drives free search-engine traffic to Dakota's Gumroad printable products.

**Status: PUBLISHED 2026-10-01 (Dakota approved).** Live at
https://dakotamccall200-create.github.io/hearthside-printables/ via GitHub Pages
(repo: dakotamccall200-create/hearthside-printables, branch main).
Deploys: edit in `~/workspace/traffic-engine/`, re-run build scripts, push to main.

## What's here

| File | Purpose |
|---|---|
| `index.html` | Homepage — hero, free-sample cards, 5 product cards, how-it-works, FAQ |
| `free-printable-budget-tracker.html` | Article + free budget tracker & bills tracker downloads |
| `printable-cleaning-schedule.html` | Article + free cleaning checklist & meal planner downloads |
| `toddler-tracing-worksheets.html` | Article + free tracing shapes & lines downloads |
| `christmas-coloring-pages.html` | Article + free tree & snowman coloring pages |
| `weekly-meal-planner-printable.html` | Article + free meal planner & budget tracker downloads |
| `monthly-bills-tracker.html` | Article + free bills tracker & budget tracker downloads |
| `freebies/` | 8 real downloadable freebies (US Letter PDFs) + PNG previews, generated with PIL |
| `images/` | Product cover art + a generated spreadsheet-bundle cover |
| `fonts/` | Bundled TTFs (Bebas Neue, Montserrat, Caveat) — loaded locally via `@font-face`, no Google Fonts |
| `sitemap.xml`, `robots.txt` | SEO plumbing |

## The 8 free samples (in `freebies/`)

`budget-tracker-sample.pdf`, `cleaning-schedule-sample.pdf`, `tracing-shapes.pdf`,
`tracing-lines.pdf`, `christmas-tree-coloring.pdf`, `christmas-snowman-coloring.pdf`,
`meal-planner-sample.pdf`, `bills-due-sample.pdf` — each with a `-preview.png` thumbnail.
Deliberately simpler than the paid packs so the paid products stay worth buying.

## Before publishing — Dakota must do these

1. **Product links are LIVE on Payhip (done 2026-10-01).** Every product button now points to
   its real Payhip URL (https://payhip.com/b/...). No placeholders remain.
2. **Pick a domain** and replace `https://www.example-replace-me.com` in
   `build_site.py` (the `DOMAIN` variable), then re-run the build so `sitemap.xml`,
   `robots.txt`, and canonical tags are correct.
3. **Give explicit approval to publish.** Nothing here has been deployed anywhere and no
   accounts were created.

## Rebuilding

- Freebies: `python3 ~/workspace/traffic-engine/build_freebies.py`
- Pages: `python3 ~/workspace/traffic-engine/build_site.py`
- Then re-verify links with the check used at build time (all internal links resolve,
  one H1 per page, unique titles/meta descriptions).

## $0 hosting options (free tiers, no card required for the free plans)

- **Cloudflare Pages** — drag-and-drop the `site/` folder; free, fast CDN, free SSL.
- **GitHub Pages** — push the `site/` folder to a repo; free hosting on `*.github.io`.
- **Netlify** — drag-and-drop the `site/` folder; free tier with SSL.

Any of these serves a static folder like this one directly. A custom domain is optional
(roughly $10–12/year at Cloudflare/Porkbun — **ask Dakota first; do not buy anything**).

## Notes

- All article copy is original; no fake reviews, no "best/#1" claims, no keyword stuffing,
  no copyrighted characters or text.
- The site name "Hearthside Printables" is a working brand — rename freely before launch.
- Freebies are marked for personal use; paid packs are sold via Gumroad only (Etsy killed per Dakota).
