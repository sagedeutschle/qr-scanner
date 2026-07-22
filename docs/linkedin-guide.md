# LinkedIn portfolio kit for `qr-scanner`

Everything you need to showcase this project on LinkedIn: click-by-click
steps, ready-to-paste text, and the media files in this folder.

> **Heads up:** LinkedIn has no "sign in with GitHub" sync — it dropped
> third-party app integrations years ago. "Connecting" GitHub to LinkedIn
> means linking your GitHub from the right places on your profile so it looks
> intentional and polished. That takes about ten minutes with the steps below.

## Files in this kit

| File | What it's for |
| --- | --- |
| `linkedin-banner.png` | Your LinkedIn profile background banner (1584×396) |
| `screenshots/desktop.png` | Hero image — the app decoding a QR code on desktop |
| `screenshots/mobile.png` | The app on a phone-sized screen |
| `social-preview.png` | Card GitHub shows when the repo is linked anywhere |

All three are watermarked "© 2026 Sage Deutschle", so they stay attributed to
you wherever they're re-shared.

## One-time GitHub setup

1. **Set the repo's social preview.** On GitHub open
   `sagedeutschle/qr-scanner` → **Settings** → **General** → scroll to
   **Social preview** → **Edit** → upload `docs/social-preview.png`.
   From then on, pasting the repo link into LinkedIn (or anywhere) shows your
   branded card — including a scannable QR code that opens the repo. Very
   on-brand for a QR scanner.
2. **Pin the repo on your GitHub profile.** On your profile page →
   **Customize your pins** → tick `qr-scanner`. Recruiters who follow your
   LinkedIn link land on your best work first.

## LinkedIn, step by step

### 0. Set your profile banner

Profile → hover the background area → **camera / edit icon** at the top-right of
the banner → **Add photo** → upload `linkedin-banner.png`. It's already sized to
LinkedIn's 1584×396 spec, with all text kept clear of where your profile photo
sits, so nothing important gets covered.

### 1. Put GitHub in your contact info

Profile → **Contact info** → pencil icon → **Website** → add
`https://github.com/sagedeutschle` and pick **Portfolio** as the type.

### 2. Feature the project at the top of your profile

Profile → **Add profile section** → **Recommended** → **Featured** → **+** →
**Add a link** → paste `https://github.com/sagedeutschle/qr-scanner`.
The card uses the social preview you set above. You can also feature the live
demo: `https://sagedeutschle.github.io/qr-scanner/`.

### 3. Add it as a Project (this is where the screenshots go)

Profile → **Add profile section** → **Additional** → **Add projects**.

- **Project name:** `QR Scanner — in-browser QR code scanner`
- **Description:** paste from the copy kit below.
- **Skills:** JavaScript, HTML/CSS, Web APIs, Responsive Design
- **Media:** upload `screenshots/desktop.png` and `screenshots/mobile.png`.
- **Link:** `https://sagedeutschle.github.io/qr-scanner/`

### 4. Add the skills so search finds you

Profile → **Add profile section** → **Core** → **Add skills**: JavaScript,
Front-End Development, Web Development. Tag the QR Scanner project on each
skill so the project shows as proof.

## Copy-paste kit

**Project description (for the Projects section):**

> A QR code scanner that runs entirely in the browser — one HTML file, no
> backend, no build step, nothing to install. It uses the native
> BarcodeDetector API where available and falls back to the jsQR library
> everywhere else, so it works across Chrome, Safari, and Firefox, on desktop
> and mobile. Nothing ever leaves the device: no network requests, no
> analytics, and it works offline. Built with plain JavaScript and modern CSS.

**Headline add-on (append to your current headline):**

> Building small, dependency-free web tools · JavaScript

**About-section paragraph (drop into your About):**

> I like building small tools that respect the user: my in-browser QR scanner
> is a single HTML file with zero dependencies — it scans from the camera
> using the native BarcodeDetector API (with a jsQR fallback), runs offline,
> and sends nothing to any server. Code and live demo are on my GitHub:
> github.com/sagedeutschle/qr-scanner

**Optional announcement post (attach both screenshots):**

> Small tools can still be well-made tools. I built a QR code scanner that is
> one HTML file: no backend, no build step, no dependencies. It uses the
> browser's native BarcodeDetector API when available and falls back to jsQR
> when it isn't, so it works basically everywhere — and nothing ever leaves
> your device.
>
> Try it in your browser: https://sagedeutschle.github.io/qr-scanner/
> Code: https://github.com/sagedeutschle/qr-scanner

## Protecting your work

- **The screenshots are watermarked** with your name and the repo URL, so
  re-posts stay attributed. The social preview card carries your copyright
  line too.
- **The MIT license requires attribution**: anyone reusing the code must keep
  your copyright notice. (Note: MIT does permit commercial use — your README
  asks people not to sell it, but that's a request, not a legal term. If you
  ever want "free for personal use, no selling" to be enforceable, switch to
  a license like PolyForm Noncommercial — happy to set that up.)
- **Your git history is your proof of authorship.** Every commit is
  timestamped under your account; if someone claims your work, the record
  says otherwise.
- **LinkedIn media is display-only** — uploading screenshots there grants
  LinkedIn a hosting license but transfers no ownership, and viewers get no
  rights to your code.
