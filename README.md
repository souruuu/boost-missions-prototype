# Boost Missions — Clickable Prototype

Demo prototype for GrabSpark 2026 (concept screens with sample data; the 30% fee is an example rate, not Grab policy).

**Live demo:** https://souruuu.github.io/boost-missions-prototype/

## Why the files are split

`index.html` (a copy of `Viewer.dc.html` plus a mobile layout) loads the five screens (`Main`, `Choose`, `Limits2`, `Run`, `Result` — `*.dc.html`) at runtime with `fetch()`. They must be served together over HTTP; opening a single file, or `file://`, will not show every step. GitHub Pages serves the whole folder, so just share the link/QR.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000/
```

## Files

- `index.html` — entry point (5-step viewer, mobile-friendly)
- `Viewer.dc.html` — original viewer, unchanged
- `Main / Choose / Limits2 / Run / Result .dc.html` — the five screens
- `support.js`, `vendor/` — runtime (React) that renders the `.dc.html` components
