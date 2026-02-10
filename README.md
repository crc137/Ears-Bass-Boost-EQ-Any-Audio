# Ears: Bass Boost, EQ Any Audio!

Chrome extension that lets you apply a live equalizer (EQ) to audio from the active tab.  
This repository is MV3-based and uses an offscreen document for Web Audio processing.

## Features
- 11‑band EQ with gain control
- Preset save/import/export
- Spectrum visualizer
- Works on the current tab via `tabCapture`

## Structure
- `manifest.json` — MV3 manifest
- `views/popup.html` — UI
- `styles/` — CSS + fonts
- `scripts/` — popup logic, background audio, service worker
- `views/offscreen.html` — offscreen audio context host

## Local Development
1. Open Chrome and go to `chrome://extensions`.
2. Enable **Developer mode**.
3. Click **Load unpacked** and select this project folder.

## Notes
- Audio processing happens in `scripts/bg.js` within an offscreen document.
- The service worker `scripts/sw.js` proxies tab capture and runtime messages.
