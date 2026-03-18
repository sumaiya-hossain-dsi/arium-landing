# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static landing page for **Arium Immigration** (ariumimmigration.ca), hosted via GitHub Pages. The site is served from the `docs/` directory. Based on the "Dimension" template by HTML5 UP.

## Serving Locally

The site uses AJAX to load section content, so it requires a local server (cannot be opened as a plain file). From the `docs/` directory:

```bash
cd docs
npx serve .
```

## Architecture

The site is a single-page application with **modular section loading**:

- `docs/index.html` — Main entry point. Loads all sections dynamically via jQuery AJAX at startup, then fires a `sectionsLoaded` event.
- `docs/sections/<name>/index.html` — Each nav section (`intro`, `services`, `about`, `contact`, `elements`) is a standalone `<article id="...">` fragment fetched and appended into `#main`.
- `docs/assets/js/main.js` — Controls all navigation behavior: shows/hides articles with animated transitions triggered by URL hash changes, sets up close buttons, handles `sectionsLoaded` event to re-initialize articles after AJAX load.
- `docs/assets/css/main.css` — Compiled CSS (do not edit directly; source is in `docs/assets/sass/`).
- `docs/assets/sass/` — SASS source organized into `base/`, `components/`, `layout/`, and `libs/`.

## Navigation Model

Clicking a nav link (e.g. `#about`) changes `location.hash`, which triggers `hashchange` → `$main._show(id)`. The header/footer hide and the matching `<article>` animates in. Clicking outside or pressing Escape hides it.

## Booking / Calendly Integration

The "Book a consultation" button opens a **two-step modal flow** defined entirely in `docs/index.html`:
1. `#consultation-selection-modal` — user picks 20-min ($70 CAD) or 40-min ($120 CAD).
2. `#calendly-modal` — embeds a Calendly inline widget pointed at `https://calendly.com/ariumimmigration-info/{duration}mins`.

The Calendly URL slug pattern is `{duration}mins` (e.g. `20mins`, `40mins`).

## Key Content Files

| File | Content |
|------|---------|
| `docs/sections/about/index.html` | Consultant bio (Sumaiya Hossain, RCIC #R1041075) |
| `docs/sections/services/index.html` | Immigration services list (PR, temporary residency, citizenship) |
| `docs/sections/contact/index.html` | Contact info (info@ariumimmigration.ca, Toronto) |
| `docs/index.html` | Header text, nav, booking modal, consultation prices |

## Deployment

GitHub Pages serves the `docs/` folder on the `main` branch. The CNAME (`docs/CNAME`) points to the custom domain. Changes pushed to `main` deploy automatically — no build step required. CSS is pre-compiled and committed.

## Adding a New Section

1. Create `docs/sections/<name>/index.html` with `<article id="<name>">...</article>`.
2. Add `'<name>'` to the `sections` array in `docs/index.html` (around line 401).
3. Add a `<li><a href="#<name>">Label</a></li>` to the nav in `docs/index.html`.
