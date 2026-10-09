# My Day OS — Mobile Release v9

## Changes
- Prayer alarm defaults to the Mishary Rashid Alafasy Adhan recording linked from AlAdhan's public Adhan download page.
- On first use, the app attempts to download and cache the audio in IndexedDB on the user's device for offline playback. If cross-origin caching is blocked, it streams from the source when online.
- Optional custom Adhan file upload remains available.
- The recording itself is not bundled into this public GitHub repository; the app retrieves it from its host.
- Preserves existing `my-day-os-v1` task data and the v8 annual calendar.

## Source
AlAdhan download page lists “Yet Another Adhan by Mishary Rashid Alafasy”: https://aladhan.com/download-adhans

## Update
Back up data via Settings → Export. Upload `index.html`, `sw.js`, `manifest.json`, and `README.md` to the repository root and commit to `main`.
