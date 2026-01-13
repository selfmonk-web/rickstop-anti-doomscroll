# RickStop — Anti-Doomscroll Lock (Chrome Extension)

RickStop is a privacy-first Chrome extension that detects doomscrolling patterns and enforces a short “hard lock” (default 10 minutes) on supported social sites. It’s intentionally minimal: no accounts, no analytics, no remote servers.

## Why
Doomscrolling is optimized to be infinite. Your time isn’t.

RickStop breaks “scroll trance” with:
- a short lock timer
- a clear, minimal overlay
- an optional soft nudge before the lock

## Features
- **Hard lock** (default 10 minutes) with a fullscreen overlay
- **Meme only on the first lock of the day** (3 randomized variants)
- **Toolbar popup**: status, legend, stats, quick access to Options, support link
- **Options page**: lock minutes, whitelist, site toggles, sensitivity
- **20 sensitivity levels** (1 = ultra calm, 20 = aggressive)
- **Anti-bypass for slow scrolling** on low sensitivity levels (prevents “scroll slowly forever”)
- **High-level warmup gate** (for levels 12–20) to reduce false positives
- **Local-only stats**: minutes saved, streak, total saved
- **Whitelist + smart toggles**:
  - YouTube `/watch` (tutorial/single videos)
  - Reddit `/comments` (reading posts)
  - Discord (work/chat)

## Supported Sites
Out of the box (configurable by whitelist/toggles):
- YouTube, Instagram, Facebook
- X (Twitter), Reddit
- TikTok (web), Discord (web)

> Note: If a Chromebook opens a site inside an Android app, Chrome extensions can’t run there. Use the web version in Chrome.

## Install
### Chrome Web Store
- Coming soon

### Developer (unpacked)
1. Download / clone this repository
2. Go to `chrome://extensions`
3. Enable **Developer mode**
4. Click **Load unpacked**
5. Select the project folder

## Usage
- Browse normally.
- If doomscrolling patterns are detected, RickStop locks the current host for the configured time.
- When locked, there is no in-page “unlock” button.

## Configuration (Options)
Open:
- Chrome Extensions page → RickStop → **Extension options**
or
- Click the toolbar icon → **Options**

Settings:
- Lock minutes
- Sensitivity (1–20)
- Soft nudges on/off
- Whitelist hosts
- Built-in toggles (YouTube `/watch`, Reddit `/comments`, Discord)

## Privacy
RickStop is local-only and privacy-first.
- No tracking
- No analytics
- No remote servers
- No accounts

See: `PRIVACY.md`

## Project Structure
- `manifest.json` — Manifest V3 config
- `background.js` — lock state + daily meme flag + local stats
- `content.js` — doomscroll detection + overlay UI
- `popup.html / popup.js` — toolbar popup UI
- `options.html / options.js` — options UI
- `icons/` — extension icons

## Contributing
Issues and PRs are welcome.
- Please describe the problem clearly (site, device, sensitivity level, reproduction steps).
- If reporting false positives, include your sensitivity level and whether you were scrolling with mouse wheel or trackpad.

## Roadmap (Ideas)
- Per-site sensitivity
- Optional schedules (“work hours mode”)
- Better site packs (minimal, curated defaults)

## License
Choose a license (recommended for open-source): MIT.

## Support
If RickStop saves you real time, consider supporting development:
- Buy Me a Coffee: https://buymeacoffee.com/nightintel
