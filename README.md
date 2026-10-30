# Wedding invitation: Monika & Kiran

A static web page (plain HTML + CSS + JavaScript). There is no framework and no build step.

## Files

- `index.html`: the whole page (markup, styles and script in one file)
- `assets/invite-open.mp4`: opening video (envelope, seal, golden burst) with its own sound
- `assets/invite-loop.mp4`: audio-only loop that plays after the envelope opens
- `assets/poster.jpg`: first frame shown before the video is tapped
- `assets/last.jpg`: photo shown behind the first-page text
- `assets/couple.jpg`: photo behind the "Our favourite chapter begins" section
- `package.json`: optional, only provides `npm start`

## Run locally (free)

Serve the folder over http. Do not just double-click `index.html`: browsers block
the audio loop from loading when a page is opened as a `file://` address.

**Option A: Python (already installed on most computers)**
1. Open a terminal in this folder.
2. Run: `python3 -m http.server 8000` (on Windows: `py -m http.server 8000`)
3. Open http://localhost:8000 in Chrome or Safari. For the phone-sized layout,
   use the browser's device toolbar (Chrome: F12, then Ctrl+Shift+M).

**Option B: Node.js**
1. Install Node.js from https://nodejs.org (free).
2. In this folder run: `npm start` (this runs `npx serve`), then open http://localhost:8000

**Option C: VS Code**
Install the free "Live Server" extension, right-click `index.html`, choose "Open with Live Server".

To test on your phone, connect it to the same Wi-Fi and open `http://<your-computer-ip>:8000`.
Audio and video start only after a tap, which is a browser rule.

## Things you can edit (all in `index.html`)

- Names, date and venue: search for `Monika`, `Kiran`, `Aura | Area 83 Resort`
- Muhurtham time: set `var TIME="";` near the top of the script, e.g. `var TIME="Muhurtham 9:00 AM";`
- Countdown date: the line with `new Date('2026-11-20T00:00:00+05:30')`
- Timings after you tap: `4.8` (photo fades in), `5.5` (music starts), `5.9` (text appears)
  inside the `timeupdate` handler
- Colours: maroon is `#6b1426`, cream is `--cream` in `:root`
- Fonts load from Google Fonts, so they need an internet connection

## Publish for free

Upload this folder as is to any static host: Netlify Drop (https://app.netlify.com/drop),
GitHub Pages, or Cloudflare Pages. Share the link it gives you.
