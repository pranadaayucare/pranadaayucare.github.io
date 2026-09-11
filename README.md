# pranadaayucare.github.io

Static one-page site for Pranada Ayucare, an Ayurveda wellness center in Koovappady, Kerala.

Live site: https://pranadaayucare.github.io/

## Structure

```
index.html          all markup, styles (Tailwind CDN) and content
images/              photos and logo used by the site
og.png               social preview image
robots.txt, sitemap.xml, .nojekyll

assets/              source assets (originals, kept for reference/future edits)
  logo.png
  og.png
  Treatments/        treatment photos
  Yoga Images/        yoga/meditation photos
```

The site is plain HTML/CSS/JS — no build step, no dependencies to install. Tailwind is loaded from its CDN and configured inline in `index.html`; icons come from the Lucide CDN.

## Updating the site

Edit `index.html` directly. If you swap in a new photo or logo, drop the file under `images/` and update the matching `src` attribute.

## Deployment

This repo is a GitHub user Pages site (`pranadaayucare/pranadaayucare.github.io`), so GitHub Pages serves the repo root on `main` automatically — no extra settings needed.

1. Push changes to `main`.
2. The site rebuilds automatically and goes live at the URL above within a minute or two.
