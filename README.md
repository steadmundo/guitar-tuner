# Guitar & Ukulele Tuner

A simple, dependency-free web tuner. Works in any modern browser (mic access requires HTTPS or localhost).

## Features
- **Guitar mode** - standard tuning (E2 A2 D3 G3 B3 E4), tap a string or use Auto
- **Ukulele mode** - standard reentrant tuning (G4 C4 E4 A4)
- **Chromatic mode** - detects any note
- Needle meter with cents deviation, in-tune glow at +/-5 cents
- Pitch detection via normalized autocorrelation with parabolic interpolation
- Single self-contained `index.html` - no build step, no dependencies

## Deploy to Cloudflare Pages
1. Cloudflare dashboard -> Workers & Pages -> Create -> Pages -> **Connect to Git**
2. Select this repository
3. Build settings: **Framework preset: None**, build command empty, output directory `/`
4. Deploy - you get a `*.pages.dev` HTTPS URL

## Local development
Any static server works, e.g.:
```bash
npx serve .
# or
python3 -m http.server 8000
```
`(localhost is a secure context, so the mic works.)`
