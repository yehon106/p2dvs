# p2dvs

**Paste anywhere, it downloads.**

A single-page web tool: press `Ctrl+V` (or drag a file in) and it downloads instantly, guessing the right file extension automatically.

Live at: [p2dvs.vercel.app](https://p2dvs.vercel.app)

## Features

- **Auto-detect** — text is sniffed for JSON, HTML, CSV, Markdown, or falls back to `.txt`. Images convert between `.png` / `.jpg` / `.webp`. Real files (videos, 3D models, anything else) keep their original extension.
- **Manual override** — dropdown to pick a specific format, or type your own custom extension.
- **Image resize** — optionally downscale pasted images to 1920 / 1280 / 800px max before saving.
- **Drag-and-drop** — drop a file anywhere on the page as an alternative to pasting.
- **Native Save dialog** — lets you rename the file and pick where it goes (falls back to a normal download if your browser doesn't support it).
- **Session history** — the last 10 things you've saved this session, with one-click re-download and multi-select zip download.
- **Sound + vibration feedback**, **light/dark theme toggle**, **paste counter**.

## Tech

Plain HTML/CSS/JS, no build step, no dependencies except [JSZip](https://stuk.github.io/jszip/) (loaded via CDN for the zip-download feature). Fonts: Space Grotesk + IBM Plex Mono via Google Fonts.

## Deploying

This repo auto-deploys to Vercel on every push to `main`. To update the live site:

```
git add index.html
git commit -m "describe your change"
git push
```

Vercel picks it up within about a minute.

## Local dev

Just open `index.html` in a browser — no server or build step required.
