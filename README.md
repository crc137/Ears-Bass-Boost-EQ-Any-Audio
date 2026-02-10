<div align="center">
  <a href="https://github.com/coonlink">
    <img width="90px" src="image/logo.128.png" alt="Ears: Bass Boost, EQ Any Audio! Logo" />
  </a>
  <h1>Ears: Bass Boost, EQ Any Audio!</h1>

<img alt="last-commit" src="https://img.shields.io/github/last-commit/crc137/Ears-Bass-Boost-EQ-Any-Audio?style=flat&amp;logo=git&amp;logoColor=white&amp;color=0080ff" style="margin: 0px 2px;">
<img alt="repo-top-language" src="https://img.shields.io/github/languages/top/crc137/Ears-Bass-Boost-EQ-Any-Audio?style=flat&amp;color=0080ff" style="margin: 0px 2px;">
<img alt="repo-language-count" src="https://img.shields.io/github/languages/count/crc137/Ears-Bass-Boost-EQ-Any-Audio?style=flat&amp;color=0080ff" style="margin: 0px 2px;">
<img alt="version" src="https://img.shields.io/badge/version-1.4.0-blue" style="margin: 0px 2px;">

</div>

<br />

<div>
  <p>Chrome extension that lets you apply a live equalizer (EQ) to audio from the active tab.</br> 
This repository is MV3-based and uses an offscreen document for Web Audio processing.</p>
  <img width="600" src="https://raw.coonlink.com/cloud/Ears-Bass-Boost-EQ-Any-Audio.png" alt="Ears: Bass Boost, EQ Any Audio!" />
</div>

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
