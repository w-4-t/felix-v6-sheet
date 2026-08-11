# Felix Deaqur — VTM v6 Mobile Sheet v0.2 PWA

This folder is ready to publish directly with GitHub Pages.

## Files

- `index.html` — app
- `manifest.webmanifest` — PWA metadata
- `service-worker.js` — offline cache
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — app icons
- `.nojekyll` — tells GitHub Pages to serve the folder as plain static files

## GitHub Pages deployment

1. Create a new GitHub repository, for example `felix-v6-sheet`.
2. Upload **all files in this folder to the repository root**.
3. Open the repository's `Settings`.
4. Open `Pages`.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch `main` and folder `/ (root)`, then Save.
7. Wait for the Pages deployment to finish.
8. Open the published Pages URL on the iPhone in Safari.
9. Safari → Share → **Add to Home Screen** → enable/open as web app if shown.

## Offline behavior

Open the published app successfully at least once while online.
The service worker then caches the app shell. Character state is stored locally in browser/web-app storage.

## Privacy

GitHub Pages publishes a web site. Do not add private campaign notes, secrets, personal data,
or ST-only scenario material to this repository unless you are comfortable with the site being web-accessible.

The current package contains only the fictional Felix character sheet/roller.

## v0.2 scope

This is primarily v0.1 converted into a proper installable PWA. Mechanics have intentionally not
been expanded substantially yet; first test the mobile UX and installation flow.
