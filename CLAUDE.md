# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio/landing page for Hillary Hartley (`hillaryhartley.com`), hosted on GitHub Pages. There are no build tools, frameworks, or package managers — it's pure HTML and CSS deployed directly from the main branch.

## Development

No build step required. Edit `index.html` and `styles.css` directly. Changes go live when pushed to `main`.

To preview locally, open `index.html` in a browser or use any static file server:
```
python3 -m http.server
```

## Architecture

The entire site is two files:

- **`index.html`** — Single page with four sections: header (photo + social icons), bio, media & writing, and links ("Elsewhere")
- **`styles.css`** — All styles, using CSS custom properties for colors and a 560px breakpoint for the mobile→desktop layout shift

### CSS Variables (in `styles.css`)
Colors, spacing, and typography are controlled via CSS custom properties at the `:root` level. Two Google Fonts are loaded: **Inter** (body) and **Playfair Display** (headings).

### Media Section Structure (`index.html`)
The media section organizes items by era/role (Thought Leadership, USDR, Ontario Digital Service, etc.). Each item uses an inline SVG icon to indicate type (article / video / podcast) and links to an external source.

### Social Icons
Social links in the header use inline SVGs. The "Elsewhere" links section at the bottom mirrors these with text labels.

## Deployment

Push to `main` → GitHub Pages serves automatically. The `CNAME` file maps to `hillaryhartley.com`.
