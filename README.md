# QR Scanner

> Just stuff I thought would be useful for the things I want to do. If you think they will be useful for you too feel free to use them as well, just PLEASE dont try and sell it, helpful code should be for everyone. If you use this as a part of another free program credit would be nice smile :).

A tiny browser-based QR code scanner. One HTML file, one bundled JS library, no
backend, no build step, no dependencies to install.

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Zero dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)](./index.html)
[![No build step](https://img.shields.io/badge/build-not%20needed-blue.svg)](./index.html)

[**▶ Try the live demo**](https://sagedeutschle.github.io/qr-scanner/)

[![The scanner detecting and decoding a QR code](./docs/screenshots/desktop.png)](https://sagedeutschle.github.io/qr-scanner/)

## Features

- **Scans straight from your camera** — point it at a QR code and the decoded
  text lands in a copy-friendly field.
- **Native-first decoding** — uses the browser's built-in
  [`BarcodeDetector`](https://developer.mozilla.org/en-US/docs/Web/API/BarcodeDetector)
  API when available (Chromium, recent Safari), so scanning is fast and
  battery-friendly.
- **Works everywhere else too** — falls back to
  [jsQR](https://github.com/cozmo/jsQR) (vendored as `jsQR.min.js`) on browsers
  without `BarcodeDetector`.
- **Camera picker** — a dropdown selects between multiple cameras, handy on
  laptops with several webcams or phones with front/back lenses.
- **Responsive** — the same file works on desktop and phones, and long camera
  device names can't break the layout.
- **Private by design** — nothing ever leaves your device. No network requests,
  no analytics, no backend. It even works offline.

<p align="center">
  <img src="./docs/screenshots/mobile.png" alt="The scanner running on a phone-sized screen" width="300">
</p>

## Use it locally

Open `index.html` in a modern browser. That's it — `file://` is a secure context,
so the camera API works without a server.

If you'd rather serve it (e.g. from a phone on the same Wi-Fi), use HTTPS or
`localhost` — browsers refuse camera access from plain HTTP on a LAN IP.

```sh
# from inside the repo
python3 -m http.server 8000
# then open http://localhost:8000 on the same machine
```

## How it works

- Uses the native [`BarcodeDetector`](https://developer.mozilla.org/en-US/docs/Web/API/BarcodeDetector)
  API when available (Chromium, recent Safari).
- Falls back to [jsQR](https://github.com/cozmo/jsQR) (vendored as `jsQR.min.js`)
  on browsers that don't have `BarcodeDetector`.
- Picks the camera via a dropdown — handy on machines with multiple cameras.
- Detected text lands in a copy-friendly input field.

## Also in here: other little tools

Same deal as the scanner — each is one HTML file, no backend, no build step.
All progress/plans save in the browser and never leave your device.

### Phone Declutter

[`organize.html`](./organize.html) — a guided checklist for organizing the shiz
out of your phone: 46 concrete tasks across 11 zones (home screen, apps, photos,
storage, notifications, inbox, contacts, subscriptions, safety, habits), with
step-by-step iPhone and Android tips for each.

Live: <https://sagedeutschle.github.io/qr-scanner/organize.html>

### Home Screen Planner

[`homescreen.html`](./homescreen.html) — rearranges your apps into folders where
they belong and pretties it up. Tap in your apps (300+ app catalog with smart
categorization), it sorts them into verb-named folders (🎬 Watch, 💸 Pay, 🗺️ Go…)
on a live phone mockup with wallpaper themes, a dock, and a widget row. Tweak
anything by tapping, then follow the generated checklist to make your real
phone match — iOS/Android don't let outside software move icons, so the last
step is yours.

Live: <https://sagedeutschle.github.io/qr-scanner/homescreen.html>

### Playlist Maker for Apple Music

[`playlist.html`](./playlist.html) — reads what you've actually been playing on
Apple Music lately, shows your top artists, and builds a playlist straight into
your library. Three flavors: **On repeat** (your recent favorites), **Best of
both** (half favorites, half new songs from similar artists), or **New to me**
(almost all songs you haven't heard). Preview 30-second clips, kick out songs
you don't want, then save — it appears in Library → Playlists on your phone.

Live: <https://sagedeutschle.github.io/qr-scanner/playlist.html>

Two honest caveats, because Apple gates its API:

- You need an **active Apple Music subscription** and, one time, an
  **Apple Developer Program key** ($99/yr — sorry, Apple's rule, there is no
  free API access). The page walks you through getting one. The key is stored
  in your browser only and is used locally to sign requests to Apple — this
  stays a no-backend app; nothing goes anywhere except directly to Apple.
- Open it from the live GitHub Pages link or `localhost` (see the scanner
  instructions above) — Apple's sign-in pop-up needs a real `https://` or
  `localhost` origin, so plain `file://` won't work for this one.

Don't want to pay Apple $99? The setup screen also lists the **free**
built-in ways to get nearly the same thing (Made For You mixes, Discovery
Station, a Shortcuts recipe, Mac smart playlists) — the short version is:
Settings → Music → **Use Listening History** must be ON, then check the
Home tab of the Music app.

## License

MIT — see [LICENSE](./LICENSE). Attribution is required by the license (keep the
copyright notice), and a friendly credit is always appreciated.

Screenshots and preview images are © 2026 Sage Deutschle.
