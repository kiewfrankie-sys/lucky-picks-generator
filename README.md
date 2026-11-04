# Lucky Picks Generator 2.0 — Milestone 5

This is the final integration / PWA test build. It includes seven games, independent per-game configuration and random sources, session-only generated results, individual and all-game generation, and consolidated PDF export.

## New version 2.0 app icon

The package includes a new purple-and-gold Lucky Picks Generator 2.0 icon in 180px, 192px, and 512px sizes. The manifest, browser tab icon, and iPhone Home Screen icon reference the new artwork.

## Local testing

1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. Test game selection, independent row counts and sources, generation, individual regeneration, Generate All, clearing results, and PDF export.
4. Refresh: game selections and settings should persist; generated results should be cleared.
5. For PWA testing, deploy to HTTPS (GitHub Pages), open the site, and install it from the browser. A local `file://` preview cannot fully test service-worker installation or offline behaviour.

## Deployment to the existing GitHub repository

Replace `index.html`, `manifest.json`, and `service-worker.js`; replace the entire `icons` folder with this package's `icons` folder. Keep the existing repository and GitHub Pages URL. Commit all replacements together. The service-worker cache is `lucky-picks-v11`.

## Notes

- RANDOM.ORG access depends on browser/network CORS support. If it fails, the app reports an error and does not silently fall back to browser randomness.
- Tailwind CSS and jsPDF are loaded from CDNs; complete offline operation of these external libraries is not guaranteed.
- This app is for entertainment only. Randomly generated combinations do not improve the odds of winning.

## PDF layout refinement

The PDF layout uses a larger game header, larger combination typography, and row spacing distributed across the printable page. Number and ball sizes adapt to the selected row count (up to 20 rows) to preserve legibility and avoid overlap.


## PDF ball alignment and spacing refinement

- Toto balls are enlarged up to 24 mm and use most of the printable page width at low row counts.
- Number text is vertically centred within each ball using a corrected jsPDF text-baseline offset.
- Result rows use a compact centred block to reduce excessive gaps, with automatic scaling for 1–20 rows.
- Service-worker cache updated to `lucky-picks-v11`.


PDF refinement: increased Toto ball number typography to approximately 82% of ball diameter (with sensible minimum/maximum limits). Service-worker cache: lucky-picks-v12.
