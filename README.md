# Unit Converter

Length, area, weight, volume and flow between imperial and metric. Decimal places set with a slider (0–6), fractional-inch and feet-inch (dash notation) fields, color presets. Works offline once installed.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app |
| `manifest.json` | App name, colors and icons for install |
| `sw.js` | Service worker — offline support (network-first) |
| `icons/` | App icons (192, 512, maskable 512, Apple touch, favicon, SVG sources) |

## Deploy to GitHub Pages

1. Create a repo (e.g. `unit-converter`) and upload all files, keeping the `icons/` folder.
2. Repo **Settings → Pages → Build and deployment**: Source *Deploy from a branch*, Branch `main`, folder `/ (root)`. Save.
3. After a minute the app is at `https://<username>.github.io/unit-converter/`.

## Install on Android

Open the Pages URL in Chrome → ⋮ menu → **Install app** (or **Add to Home screen**). It opens full-screen and works without a signal.

## Updating

Edit `index.html`, then change `VERSION` at the top of `sw.js` (e.g. `unitconv-v1.1`) and push. The next time the app opens with a connection it loads the new version.

## Notes

- Settings, values and colors are stored in the browser on each device (localStorage).
- Fonts come from Google Fonts and are cached for offline use after the first load; system fonts are used if they were never cached.
