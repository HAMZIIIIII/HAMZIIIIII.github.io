# Ahmed Mansour — personal brand page, resume and CV

One self-contained HTML file. No build step, no framework, no package manager.
Open `index.html` in any browser, including offline.

**Live:** https://hamziiiiii.github.io

## What it is

The same page does three jobs:

1. **Brand page** — a stranger who got the link in a message knows in 30 seconds who I am and what I build.
2. **Resume** — roles, results and skills, scannable.
3. **CV** — press *Download CV (PDF)* (or Ctrl/Cmd+P) and a dedicated print stylesheet turns it into a 2-page A4 CV.

## Files

| Path | What it is |
|---|---|
| `index.html` | The entire site: markup, inline CSS, inline JS, three inline SVG diagrams |
| `headshot/ahmed.jpg` | The portrait. Replace this one file, same name, to change the photo |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

## Editing

- **Photo:** overwrite `headshot/ahmed.jpg`. Nothing in the HTML needs touching.
- **Footer date:** `Last updated:` is hand-written near the bottom of the body.
- **If the domain changes:** five places carry the absolute URL — `og:url`, `og:image`,
  `twitter:image`, `<link rel="canonical">` and the JSON-LD `url`/`image`.
- **Unconfirmed facts:** wrap them in `<mark class="todo" data-todo>…</mark>`. They render
  highlighted and a corner badge counts them. Delete the `REMOVE-BADGE` lines in the script
  to drop the badge permanently.

## Verified before deploy

- WCAG AA contrast on every text element, light and dark mode
- All text 12px or larger
- No horizontal scroll at 360px; diagrams scroll sideways rather than shrinking illegibly
- Print output is under 2 A4 pages, black on white
- Fallbacks for `color-mix()`, `backdrop-filter` and `:focus-visible` on older Safari
- `prefers-reduced-motion` stops the CSS animations and the SVG packet animation
- Opens offline; the only external request is one Google Fonts stylesheet, with system fallbacks
