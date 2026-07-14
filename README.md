# qr-scanner

> Just stuff I thought would be useful for the things I want to do. If you think they will be useful for you too feel free to use them as well, just PLEASE dont try and sell it, helpful code should be for everyone. If you use this as a part of another free program credit would be nice smile :).

A tiny browser-based QR code scanner. One HTML file, one bundled JS library, no
backend, no build step, no dependencies to install.

## Live demo

<https://sagedeutschle.github.io/qr-scanner/>

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

## Also in here: phone organization tools

Same deal as the scanner — each is one HTML file, no backend, no build step,
works from `file://`. All progress/plans save in the browser and never leave
your device.

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

## License

MIT — see [LICENSE](./LICENSE).
