# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static one-page marketing site for Pranada Ayucare, an Ayurveda wellness center in Koovappady, Kerala. There is no build step and no package manager — the entire site is `index.html` plus static assets, deployed via GitHub Pages.

## Architecture

- `index.html` — the whole site: all markup, styling, and content live in this single file. There is no templating or componentization; sections are plain `<section>` blocks in document order (hero → about → treatments → approach → reviews → CTA → contact → footer).
- Styling is Tailwind CSS loaded from the CDN (`cdn.tailwindcss.com`) and configured inline via a `tailwind.config` script block in `<head>` (custom colors: `background`/`cream`, `foreground`/`forest`, `saffron`, `sage`; custom `fontFamily.heading`). Edit that inline config to change the design tokens — there is no `tailwind.config.js` file.
- Icons come from Lucide via CDN (`unpkg.com/lucide@latest`), rendered with `<i data-lucide="...">` tags and initialized by `lucide.createIcons()` at the bottom of the page.
- `images/` — production images actually referenced by `index.html` (`images/logo.png`, `images/treatments/*`, `images/yoga/*`).
- `assets/` — source/original versions of images kept for reference or future re-edits; not directly referenced by the page. When replacing a photo, add the new file under `images/` (and optionally keep an original in `assets/`) and update the corresponding `src` in `index.html`.
- `og.png`, `robots.txt`, `sitemap.xml`, `.nojekyll` — SEO/social and GitHub Pages plumbing at the repo root.

## Development

There is no dev server, bundler, linter, or test suite. To work on the site, edit `index.html` directly and open it in a browser (or use a simple static file server) to preview.

## Deployment

This repo is the GitHub user Pages site `pranadaayucare/pranadaayucare.github.io`. Pushing to `main` deploys automatically — GitHub Pages serves the repo root with no build step.
