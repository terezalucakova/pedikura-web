# CLAUDE.md — Studio Hanky Víchové

## Project overview

Static one-page website for a pedicure/manicure salon in Havířov. Pure HTML5 + CSS3 + vanilla JS, no framework. Czech language, formal vykání throughout.

Live reservation system: https://studio-hanky-vichove.snippet.myfox.cz

## File structure

```
index.html        — single-page site with anchor navigation
styles.css        — all styles, CSS custom properties, responsive
script.js         — sticky nav, hamburger, smooth scroll, scroll-reveal, FAQ, back-to-top
img/
  hero-illustration.svg    — peony (3-layer: 8+8+6 petals)
  studio-illustration.svg  — arching branch with rose
  team-hanka.svg           — rose
  team-vera.svg            — daisy
  team-sylva.svg           — magnolia
  logo.png                 — salon logo
kontext.md        — full project brief (content, copy, services, pricing)
```

## Design tokens (CSS custom properties)

```css
--color-primary: #C4788E;
--color-primary-dark: #9E5470;
--color-gold: #C4A060;
--color-gold-dark: #A07840;
--color-burgundy: #8B2255;
--color-booking: #2E1E28;
```

Background: warm cream `#FAF7F2`. Section titles use `--color-burgundy`, eyebrows use `--color-gold-dark`.

## Typography

- Headings: **DM Serif Display** (Google Fonts) — switched from Cormorant Garamond because Czech diacritics were too prominent at large sizes
- Body: **Inter** (Google Fonts)

## Nav logo

Two `<span>` elements (no `<img>`):
- `.nav__logo-studio` — gold, small-caps, uppercase ("STUDIO")
- `.nav__logo-name` — burgundy serif, DM Serif Display ("Hanky Víchové")

## SVG illustrations

Hand-coded using `<g transform="rotate(X)"><path/></g>` petal rotation. No design tool needed. All share the same warm palette (dusty rose, sage green, gold accents).

## Key layout decisions

- Section padding: `clamp(40px, 5vw, 72px) 0`
- Hero has no border/box around illustration — `.hero__image-wrap` has no background, border-radius, or overflow
- All pricing card CTAs use `btn--primary` (unified, no `btn--outline` mix)
- Google Maps embed uses `?output=embed` pattern, no API key required

## Team & contacts

| Name | Role | Phone |
|------|------|-------|
| Hanka Víchová | Pedikúra | 607 170 843 |
| Věra Pavlíková | Pedikúra | 722 537 456 |
| Sylva Hottková | Manikúra + masáže | 737 270 804 |

## Deployment

No git repo yet. Deploy target: GitHub → Vercel (auto-deploy).
