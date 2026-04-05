# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static marketing website for **Block Blast Frozen**, a mobile puzzle game by **Vedrix Labs**. No build system, bundler, or framework — just plain HTML/CSS/JS served as static files.

## Architecture

- **index.html** — Main landing page with inline CSS and JS. Contains hero section, features, app store links, and snowfall animation. Uses CSS custom properties for the frost/ice theme (defined in `:root`).
- **privacy-policy.html** — Privacy policy page (standalone, inline styles).
- **terms-of-use.html** — Terms of use page (standalone, inline styles).
- **assets/** — Static images (logo, etc.).

All three pages duplicate the shared CSS theme variables and nav/footer markup inline — there is no shared stylesheet or template system.

## Development

No build step. Open HTML files directly in a browser or serve with any static file server:

```
python3 -m http.server 8000
```

## Design System

Font: Inter (loaded from Google Fonts). Color palette uses CSS custom properties: `--navy`, `--ice-blue`, `--ice-teal`, `--ice-violet`, `--frost-white`, etc. defined in each file's `:root`.
References: Use images in the references folder for creating design and assets as these images are of real gameplay. Do not directly reference anything from references folder as this won't be committed, rather copy it in assets if you want to use something directly
