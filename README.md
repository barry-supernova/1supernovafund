# Supernova Fund website

Static site for https://1supernovafund.com. No build step, no framework, no server code.

## What's here
- `index.html`: every page, style and script in one file.
- `img/`: all images the site uses (logos, portfolio and team photos, press images, favicon, social share image).
- `robots.txt` and `sitemap.xml`: for search engines.

## Deploy
1. Upload the whole folder as-is to the web root for 1supernovafund.com (Netlify, Vercel, Cloudflare Pages, S3 or the existing host). Keep `img/`, `robots.txt` and `sitemap.xml` next to `index.html`.
2. Make sure the site is served over HTTPS and that `www.1supernovafund.com` redirects to `https://1supernovafund.com/` (or the reverse), so there is one canonical address.
3. Submit `https://1supernovafund.com/sitemap.xml` in Google Search Console and Bing Webmaster Tools.

To preview locally: run `python3 -m http.server` inside this folder, then open http://localhost:8000.

## SEO already in place
- Descriptive title and meta description, canonical URL, `robots` meta.
- Open Graph and Twitter card tags with a 1200x630 share image (`img/og-image.jpg`), so links preview properly on LinkedIn, iMessage, Slack and X.
- Structured data (JSON-LD) for the organization and website.
- Favicon and Apple touch icon.
- Alt text on all meaningful images; below-the-fold images lazy-load.
- Mobile viewport tag; layout tested at 360, 390, 768 and desktop widths with no horizontal scrolling.

If the domain is not 1supernovafund.com, search for `1supernovafund.com` in `index.html`, `robots.txt` and `sitemap.xml` and replace it.

## How it works
- Pages are hash routes in one file: `#home`, `#companies` (Portfolio), `#experience`, `#team`, `#manifesto`, `#news`. All copy is in the HTML, so search engines index the full site as one page.
- Optional later upgrade for SEO: split each view (`<div class="view" id="v-...">`) into its own page (/portfolio, /team, etc.) so each can rank separately with its own title and description.
- Animations (hero star dust trail, founder constellation, scroll reveals, spinning stars) live in the inline scripts at the bottom of `index.html`. All of them respect the visitor's "reduce motion" setting.
- News items are in the `NEWS` array near the bottom of the script. Add `url:` to an item to make it a link.

## Fonts
- Instrument Serif and Instrument Sans load from Google Fonts.
- The footer tagline is set in PP Telegraf to match 1supernova.com. Add the licensed PP Telegraf web font files (the same ones 1supernova.com uses) with an `@font-face` rule named "PP Telegraf". Until then it falls back to Instrument Sans.

## Optional
- Add analytics (Plausible, Fathom or GA4) before launch if you want traffic data.

## Outbound links
- Apply: https://nova.1supernova.com
- Intro call: https://calendly.com/supernova-intro/supernova-intro
- Contact: christopher@1supernova.com
