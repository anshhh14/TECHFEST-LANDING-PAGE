# Techfest — Landing Page Concept

A concept landing page for Techfest, designed around a "mission control"
idea — the festival as a launch, with a live countdown console and
telemetry-style stats instead of the usual hero banner + stock photo grid.

## Structure

```
techfest-landing/
├── index.html        page markup
├── css/style.css      design system + layout
├── js/main.js          countdown, starfield canvas, scroll reveals, counters
└── README.md
```

No build step, no dependencies beyond Google Fonts. Just open `index.html`
in a browser, or serve the folder with anything static (`npx serve`,
`python3 -m http.server`, GitHub Pages, Netlify drop, etc).

## Design notes

- **Palette** — deep navy hull (`#0a0f1c`) with amber (`#ffb13d`) as the
  primary signal color and cyan (`#52d8c9`) as the secondary one. Read
  as instrument-panel lighting rather than a generic dark-mode gradient.
- **Type** — Space Grotesk for display headings, IBM Plex Sans for body
  copy, IBM Plex Mono for anything that reads like data (the countdown,
  stat labels, section tags).
- **Signature element** — the console panel in the hero: a live countdown
  to opening day plus four animated telemetry stats (events, footfall,
  countries, prize pool) that count up when scrolled into view.
- Numbered "SYS/01–06" tags on the event cards and the Day 1/2/3 timeline
  are both genuinely sequential content, not decoration.

## Things to swap before this goes live

- `LAUNCH_DATE` in `js/main.js` — set to the real opening ceremony date/time.
- Copy throughout is placeholder (speaker names, event descriptions,
  sponsor names) — replace with the real lineup.
- The register form doesn't submit anywhere; wire it to whatever backend
  or form service you're using and remove the "demo build" note.
- Swap the inline SVG icons for real event photography once you have it,
  if you want a less illustrated look.

## Browser support

Modern evergreen browsers. Respects `prefers-reduced-motion` for the
starfield, scan line, and scroll reveals.
