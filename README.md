# Midnight Sudoku

A dark, glassy sudoku for iPhone, built as an installable web app (PWA). No build step: plain HTML, CSS and JavaScript.

- Four levels (Easy ~40 clues, Medium ~32, Hard ~27, Expert ~23). Every generated puzzle has exactly one solution.
- Daily puzzle (same for everyone on a given date), streaks, statistics, notes, hints, undo, mistake limit.
- Saves your game automatically; works offline once installed from an HTTPS address.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app |
| `manifest.webmanifest` | App name, colors and icons for the Home Screen |
| `sw.js` | Offline cache |
| `icons/` | App icons (180, 192, 512 px) |

## Put it on your iPhone

1. Host this folder on any HTTPS address, for example by dragging it onto https://app.netlify.com/drop (free account) or pushing it to a GitHub Pages repository.
2. On the iPhone, open that address in **Safari**.
3. Tap **Share**, then **Add to Home Screen**, then **Add**.

It now opens full screen from its own icon and keeps working without a connection.

## Try it on the iPhone over Wi-Fi (no hosting)

From this folder on the PC:

```bash
python -m http.server 8000
```

Find the PC's local IP with `ipconfig`, then open `http://<that IP>:8000` in Safari on the iPhone (same Wi-Fi). This is good for testing; offline mode only works from an HTTPS address.

## Updating

After changing files, bump `CACHE` in `sw.js` (for example `midnight-sudoku-v2`) so installed copies pick up the new version.
