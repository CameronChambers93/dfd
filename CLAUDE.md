# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static HTML/CSS/JS website for **Driveway Friendly Dumpster Inc.** — a Michigan rubber-tire dumpster rental company. Hosted on GitHub Pages.

## Structure

```
index.html          Home page
our-dumpsters.html  Dumpster sizes & specs
about.html          Company story
service-area.html   40+ Michigan communities served
get-a-quote.html    Quote request form
policies.html       Privacy policy & terms
css/style.css       All styles (single file, CSS custom properties)
js/main.js          Mobile nav toggle + active link highlighting
```

## Key Design Decisions

- **Color palette** defined as CSS variables in `:root` — `--navy`, `--gold`, `--green` are the three primary brand colors.
- **No build step** — plain HTML/CSS/JS, open any `.html` file directly in a browser to preview.
- **Quote form** on `get-a-quote.html` currently uses `action="mailto:..."` as a fallback. To enable proper submissions, swap the `action` attribute for a [Formspree](https://formspree.io) endpoint (`https://formspree.io/f/YOUR_ID`).
- **Logo** is hotlinked from the live WordPress site. If that URL breaks, replace the `<img src>` in every page's `<header>` with a locally hosted file.
- **Responsive breakpoints**: 900px (2-col → stacked) and 640px (mobile nav, single-column).

## GitHub Pages Deployment

Push to the `main` branch and enable GitHub Pages in repo Settings → Pages → Source: `main` / `/ (root)`. No build action needed.
