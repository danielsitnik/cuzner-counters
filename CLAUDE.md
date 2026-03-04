# Cuzner Counters

A humorous static website that calculates accumulated life events since April 1, 2008. Hosted at [cuzner.today](https://cuzner.today) via GitHub Pages.

## Tech Stack

- **Vanilla HTML/CSS/JavaScript** — no framework, no build step, no package manager
- **Day.js** (v1.11.10) — loaded via CDN for date math
- **Day.js pt-br locale** — loaded via CDN for Portuguese (Brazil) localization
- **GitHub Pages** — automatic deployment on push to `main`

## Project Structure

```
index.html   # All application logic (markup + inline JS)
style.css    # Styling with CSS custom properties
CNAME        # Custom domain: cuzner.today
mestre.webp  # Hero image
```

No build pipeline, no dependencies to install, no environment variables.

## Running Locally

Open `index.html` directly in a browser, or serve with any static server:

```bash
python -m http.server 8000
```

## Key Implementation Details

- **Base date:** `2008-04-01` (hardcoded in `index.html`)
- **Counter logic:** each counter multiplies a daily rate by elapsed days since the base date
- **Rates object:** 23 counters defined in the `rates` object inside `<script>` in `index.html`
- **Language:** Portuguese (Brazil), hardcoded via `dayjs.locale("pt-br")`
- **Easter egg:** on April 1st, displays a birthday/anniversary count

## Making Changes

- **Add/edit a counter:** update the `rates` object and add a corresponding `<div class="stat">` in the HTML
- **Change the base date:** update the `baseDate` constant
- **Change styling:** edit CSS custom properties at the top of `style.css`

## Testing

No automated tests. Verify changes by opening `index.html` in a browser. Deployment is automatic via GitHub Pages on merge to `main`.
