# Lucky Picks Generator — Shareable PWA

## Files
- `index.html`: the application
- `manifest.json`: installable app metadata
- `service-worker.js`: app-shell and best-effort CDN caching
- `icons/`: Home Screen icons

## Publish using GitHub Pages
1. Create a GitHub repository, e.g. `lucky-picks-generator`.
2. Upload the contents of this folder to the repository root (not the ZIP itself).
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish the site. Its URL will look like:
   `https://YOUR-USERNAME.github.io/lucky-picks-generator/`

## Install on iPhone
1. Open the published HTTPS URL in Safari.
2. Tap Share → Add to Home Screen.
3. If shown, enable **Open as Web App**, then tap Add.
4. Launch it from the new Home Screen icon.

## Important notes
- Hosting is required for sharing. This package is ready to publish, but it has not been uploaded to a public website.
- PWA installation requires HTTPS (GitHub Pages provides HTTPS).
- Open the site online at least once after deployment so the service worker can install and cache the app shell.
- The service worker attempts to cache the Tailwind and jsPDF CDN scripts. Offline PDF export depends on those CDN resources having been cached successfully.
- Pseudorandom generation runs locally. RANDOM.ORG requires internet access and may be blocked by browser CORS restrictions; this standalone front end does not include a server-side proxy.
- Anyone with the published link can access the app. Do not put private information in this public repository.
