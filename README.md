# EARTH JUKEBOX: Listen to the Living Planet
Independent NASA Space Apps Challenge project (not owned, sponsored or endorsed by NASA). BY Adham Mohammed

## Run
No install needed. Open `index.html` in Chrome, Edge or Firefox (works from a double-click), or host the folder on any static host (GitHub Pages, Netlify).

## What works now
Home, Jukebox Studio (8 datasets, live Web Audio sonification, play/pause/resume/stop/restart, seek, speed, volume, mute, waveform, live readout, text version of the data), About (method and limits), larger-text and high-contrast switches.

## Method (short)
`tools/analyze.py` reads the supplied NASA images, builds 128 column profiles (level and variability) and writes `assets/profiles.js`.
The browser maps level to a pentatonic pitch and variability to filter brightness and shimmer. All sound is synthesized; no audio files.
Every output is labelled **image-derived** because the supplied package contains no numerical data. See `docs/RESOURCE_INVENTORY.md`.

Re-run analysis: `python tools/analyze.py "<folder with the NASA images>"` (needs numpy, Pillow).
