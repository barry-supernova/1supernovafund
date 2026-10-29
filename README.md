# Supernova Fund website

Static site. No build step, no framework, no server code.

## What's here
- `index.html` contains all pages, styles and scripts in one file.
- `img/` contains every image the page uses (logos, portfolio photos, team headshots, press images).

## Deploy
Upload the folder as-is to any static host (Netlify, Vercel, Cloudflare Pages, S3, Webflow custom code, or the existing 1supernovafund.com server). Keep `img/` next to `index.html`.

To preview locally: `python3 -m http.server` inside this folder, then open http://localhost:8000.

## How it works
- Pages are hash routes in one file: `#home`, `#companies` (Portfolio), `#experience`, `#team`, `#manifesto`, `#news`.
- The hero starburst and the "founders on Earth" constellation are canvas animations in the inline script at the bottom of `index.html`. Both respect `prefers-reduced-motion`.
- News items live in the `NEWS` array near the bottom of the script. Add `url:` to an item to make the row a link.
- Fonts load from Google Fonts (Instrument Serif and Instrument Sans). Everything else is local.

## Before launch
- Add a favicon, Open Graph image and meta description for link previews.
- Add analytics if wanted.
- If you want real URLs per page (e.g. /portfolio) instead of #portfolio for SEO, the views can be split into separate HTML files; the markup for each is a `<div class="view" id="v-...">` block.

## Outbound links
- Apply: https://nova.1supernova.com
- Intro call: https://calendly.com/supernova-intro/supernova-intro
- Contact: christopher@1supernova.com
