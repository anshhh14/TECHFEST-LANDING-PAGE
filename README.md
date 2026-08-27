<div align="center">

# ⌁ TECHFEST — LANDING PAGE

### `// mission_control.log`

**A concept landing page for Techfest, built around one idea:**
**the festival as a launch, not a poster.**

![HTML5](https://img.shields.io/badge/HTML5-e34f26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572b6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)
![No Build Tools](https://img.shields.io/badge/build%20tools-none-52d8c9?style=for-the-badge)

**[▶ Live Demo](#)** · **[Report an Issue](#)** · **[Design Notes](#-design-notes)**

</div>

<br>

<div align="center">

```
STATUS: SYSTEMS NOMINAL          T-MINUS COUNTDOWN ACTIVE
EVENTS: 150+                     FOOTFALL: 180,000+
```

</div>

---

## ⌁ What this is

A single-page concept site for Techfest — dark "mission console" hero with a
**live countdown clock**, animated telemetry stats, a 2D canvas starfield,
and section-by-section reveals as you scroll. No frameworks, no build step,
no dependencies beyond two Google Fonts.

| | |
|---|---|
| 🚀 **Hero** | Live countdown to opening day + animated stat counters |
| 🛰️ **Events** | Six "system modules" — Robotics, Hackathon, Astronomy, Design Sprint, Esports, Rocketry |
| 🗓️ **Schedule** | Three-day flight plan, laid out as a timeline |
| 🎙️ **Guests** | Speaker roster with console-styled cards |
| 🤝 **Partners** | Auto-scrolling sponsor marquee |
| 📝 **Register** | Demo pass-registration form |

---

## ⌁ Stack

No framework. No bundler. No `node_modules`. Just three files and a browser.

```
HTML5   —  semantic markup
CSS3    —  custom properties, grid, clamp(), zero utility framework
Vanilla JS — countdown timer, canvas starfield, IntersectionObserver reveals
```

---

## ⌁ Folder structure

```
techfest-landing/
├── index.html          → page markup
├── css/
│   └── style.css        → design system + layout + responsive rules
├── js/
│   └── main.js           → countdown, starfield, scroll reveals, counters
└── README.md
```

---

## ⌁ Run it locally

No install, no build. Pick whichever you've got:

<table>
<tr><td>

**Just open it**
```bash
open index.html
```

</td><td>

**Python**
```bash
python -m http.server 8000
```

</td><td>

**Node**
```bash
npx serve
```

</td></tr>
</table>

Then visit `http://localhost:8000` (or whichever port your tool prints).

> Prefer VS Code? Install the **Live Server** extension → right-click
> `index.html` → *Open with Live Server*. Auto-reloads on save.

---

## ⌁ Design notes

**Direction.** Most AI-styled dark pages land on the same three looks —
warm cream + serif, black + neon accent, or a broadsheet grid. This one
takes a different reference point: an actual **instrument panel**. Amber
for primary signal, cyan for secondary, monospace type wherever something
reads like data instead of prose.

| Token | Value | Role |
|---|---|---|
| `--bg` | `#0a0f1c` | hull / base background |
| `--amber` | `#ffb13d` | primary signal, CTAs |
| `--cyan` | `#52d8c9` | secondary signal, links |
| `--display` | Space Grotesk | headings |
| `--body` | IBM Plex Sans | body copy |
| `--mono` | IBM Plex Mono | countdown, labels, stats |

**Signature element.** The console panel in the hero — a live countdown to
opening day, with telemetry stats that count up once they scroll into view.
It's the one thing this page is built around; everything else stays quiet
so that panel does the talking.

**What's genuinely sequential vs. decorative.** The `SYS/01–06` tags on
event cards and the `Day 1 / 2 / 3` timeline markers are real ordering —
not numbering for numbering's sake.

---

## ⌁ Before this goes live

- [ ] Set the real opening-ceremony date in `LAUNCH_DATE` (`js/main.js`)
- [ ] Swap placeholder speaker names, event copy, and sponsor names for the real lineup
- [ ] Wire the register form to an actual backend or form service
- [ ] Swap inline SVG icons for real event photography, if preferred

---

<div align="center">

**Browser support:** modern evergreen browsers · respects `prefers-reduced-motion`

<sub>Concept build for demo purposes — not an official Techfest / IIT Bombay property.</sub>

</div>
