# Felix Deaqur — VTM v6 Mobile Sheet v0.5 PWA

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


## v0.3 change

Copied roll results now include exact Attribute and Skill ratings and the full pool provenance.

Example:

`Strength 3 + Fighting 3 + Hand-to-Hand Focus +1 + Wrestler +1 = Raw 8, D2 → 6 dice → [9,7,8,8,4,10] → 4S, 10s:1, 1s:0, Q+1`


## v0.4

Roll Builder now separates:
- Dice modifier
- Base Difficulty
- Difficulty modifier
- Effective Difficulty

Both modifier types can have an optional reason, which is included in copied results.

Example:
`Strength 3 + Fighting 3 + Hand-to-Hand Focus +1 = Base Pool 7 -1 die (Surprised) = Pool 6; Base D2 +1 (Called Shot) = Effective D3 → 3 dice → [...]`


## v0.5

iPhone modifier entry no longer depends on the numeric keyboard.

Both:
- Dice modifier
- Difficulty modifier

now use touch-friendly steppers:

`[ − ]   0   [ + ]`

Each tap changes the value by 1, from -10 through +10. The value field is read-only, so Safari does not open a keyboard for it.
