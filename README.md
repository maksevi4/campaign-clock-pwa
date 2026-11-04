# Campaign Clock (PWA)

D&D campaign clock: time of day, custom calendar, rests, meals, per-character timed statuses.
Installable on a phone, works offline, saves to the device.

## Deploy on GitHub Pages
1. Create a repository (e.g. `campaign-clock`) and upload everything in this folder to the repo root
   (`index.html`, `manifest.json`, `sw.js`, `icons/`).
2. Repo → Settings → Pages → Build and deployment → Source: "Deploy from a branch",
   Branch: `main`, folder `/ (root)` → Save.
3. After ~1 minute the app is at `https://<your-username>.github.io/<repo-name>/`.

## Install on Android
Open the URL in Chrome → menu (⋮) → "Install app" / "Add to Home screen".

## Install on iPhone
Open the URL in Safari → Share → "Add to Home Screen".

## Updating
After changing any file, edit `sw.js` and bump `CACHE_VERSION` (`v1` → `v2`), otherwise installed
phones may keep showing the old cached version. Close and reopen the app once or twice to pick it up.

## Your data
Saved in the browser's localStorage under the key `campaign-clock-state-v1`, tied to the site address.
It is lost if you clear site data, uninstall the app, or change the URL. Use
"Backup & transfer" inside the app to export/import it (copy as text or .json file).
