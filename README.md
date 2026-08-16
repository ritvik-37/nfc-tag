# NFC Profile Card

A single-page, self-contained profile card built for an NFC tag. Tap the tag → phone opens this page → shows WhatsApp and Instagram links.

**Live:** https://ritvik-37.github.io/nfc-profile/

## Features

- Auto light/dark theme (follows phone system setting)
- Background photo baked into the page (no external image files, works offline once loaded)
- Locked by default — only opens fully when visited with the correct `?key=` in the URL (see below)
- No backend, no build step — plain HTML/CSS/JS

## How it works

The page is locked behind a simple key check:

```
https://ritvik-37.github.io/nfc-profile/?key=rr06x9k2
```

Visiting the plain URL (no key) shows a "Locked" message. The NFC tag is programmed with the full URL including the key, so tapping it unlocks the card automatically.

## Setup / Deploy

1. Fork or clone this repo
2. Edit `index.html` — change name, links, key, background image (base64-embedded)
3. Push to `main`
4. Repo → Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)`
5. Site goes live at `https://<username>.github.io/<repo-name>/`

## Writing the NFC tag

Use an app like **NFC Tools** (Android/iOS):

1. Add record → **URL/URI**
2. Paste: `https://ritvik-37.github.io/nfc-profile/?key=rr06x9k2`
3. Write to tag

> Must be a URL/URI record type, not a plain text record, or the phone won't treat it as a clickable link.

## Tech

- HTML / CSS / vanilla JS
- Fonts: Space Grotesk, IBM Plex Mono (Google Fonts)
- Hosted free on GitHub Pages

## License

MIT — free to use, modify, and share.
