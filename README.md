# Screen Ruler

A free online ruler that measures real inches and centimeters directly on your screen.

**Live site:** https://onlinescale.me/

## Why it needs calibration

Browsers only know pixels — they have no reliable way to read your display's true physical size. Two screens with identical resolutions can be very different sizes in the real world, so any ruler that assumes a fixed 96 DPI will be wrong on most modern displays.

This tool solves that with a one-time visual calibration: you hold a standard object against the screen (a credit card is the same size worldwide) and drag a slider until the on-screen shape matches it. That yields an exact pixels-per-millimeter value for your display.

## Features

- Accurate inch and centimeter scales after calibration
- One-time calibration, saved per device in `localStorage`
- Reference objects: credit card, US dollar bill, A4 paper, US Letter paper
- Automatic browser-zoom drift detection, prompting recalibration
- Fully client-side — no backend, no accounts, no tracking, nothing uploaded
- Responsive, works on desktop, tablet, and phone

## Tech

A single self-contained `index.html` — no build step, no dependencies, no framework. The ruler is drawn on a `<canvas>` at device pixel ratio for crisp rendering. Inter is loaded from Google Fonts; everything else is inline.

## Local development

No tooling required. Open the file directly:

```bash
open index.html
```

Or serve it locally:

```bash
python3 -m http.server 8000
```

## Deploying

Any static host works — GitHub Pages, Netlify, Vercel, or Cloudflare Pages. If you deploy to your own domain, update the URLs in `index.html` (canonical, `og:url`, JSON-LD), `sitemap.xml`, and `robots.txt`.

## License

MIT
