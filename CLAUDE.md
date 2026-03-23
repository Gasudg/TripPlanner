# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static travel planning website for a 25-day Europe trip (April-May 2026) covering Madrid, Barcelona, Paris, Milan, Venice, Florence, Rome, and Naples. The traveler is Uruguayan.

## Architecture

- **`index.html`** — Single-file static web app. All HTML, CSS, and JavaScript are embedded in this one file. It uses:
  - Leaflet.js (via CDN) for the interactive map
  - Google Fonts (Cormorant Garamond, Playfair Display) via CDN
  - A fixed sidebar navigation (300px wide) + scrollable main content area
  - CSS custom properties for theming (gold/warm palette: `--accent`, `--gold`, `--bg`, etc.)
  - No build system, no package manager — open directly in a browser

- **Markdown docs** — Standalone reference documents, not rendered by the HTML app:
  - `itinerario_europa.md` — Full day-by-day itinerary
  - `informacion_practica.md` — Transport, accommodation, food, budget
  - `calendario_detallado.md` — Day-by-day calendar with schedules
  - `checklist_pre_viaje.md` — Pre-trip checklist organized by timeframe
  - `resumen_ejecutivo.md` — Quick reference summary

- **`images/`** — Outfit reference images (outfit_0X_real.png are the real clothing photos; outfit_0X_v2.png and outfit_0X_smart_casual.png etc. are AI-generated illustrations). Also individual clothing item images.

## Development

No build step. To preview:
```
open index.html
```
or serve locally with:
```
python3 -m http.server 8080
```

All changes to the UI are made directly in `index.html`. The markdown files are independent documents edited separately.
