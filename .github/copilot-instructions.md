## Quick orientation — what this repo is

- This repository is a small static website (Cordillera Administrative Region final project).
- Source pages live in `code/` (HTML + `styles.css`). Assets/content appear under `content/`.
- Key files to inspect first: `code/index.html` (homepage), `code/styles.css` (global styles),
  `code/plan-your-trip.html` (form example), and the other pages in `code/` (activities, destinations, history).

## What to change and where (concrete examples)

- Change layout/markup: edit the appropriate `code/*.html` file (e.g. update header in `code/index.html`).
- Change global styling: edit `code/styles.css`. Prefer small, targeted edits; use existing selectors.
- Add images/media: place files in `content/` and reference them using relative paths from pages in `code/`.

Example: to preview a style change to the homepage

1. Open `code/index.html` in a browser OR serve `code/` with a local HTTP server (recommended).
2. In PowerShell, from the repo root or `code/` directory run:

```powershell
cd .\code
python -m http.server 8000
# then open http://localhost:8000 in a browser
```

## Project-specific patterns and constraints (do not guess)

- This is a hand-authored static site — no build system, no package.json, no bundler. Avoid introducing heavy frameworks unless requested.
- Keep changes limited to `code/` and `content/` for this project. There are other unrelated projects in the workspace (C, C++, Java folders); do not modify them unless an issue explicitly requires cross-project work.
- Use relative links; preserve the existing link structure across the pages when renaming files.

## Developer workflow / PR guidance

- Make small, focused commits with clear messages (e.g., "Update hero copy on index.html" or "Fix header spacing in styles.css").
- Include a brief manual verification checklist in PR description: pages opened, responsive check (mobile/desktop), and assets verified.

## When automating or writing code suggestions for this repo

- Prefer edits that are minimal and localized (edit the single HTML file or `styles.css` rather than regenerating the whole site).
- If adding new assets, place them under `content/` and update the referring HTML with a relative path.
- If unsure how pages link together, inspect `code/index.html` and the other `code/*.html` files — they show the site's navigation and relative linking conventions.

## Useful files to reference

- `code/index.html` — homepage, primary navigation
- `code/styles.css` — single stylesheet used across pages
- `code/plan-your-trip.html` — form + inputs (useful as an example for markup and classes)
- `content/` — media and static assets

If anything here is unclear or you'd like more detail (e.g., sample URLs used in the pages, image naming conventions, or a short preview script), tell me which area to expand and I will iterate.
