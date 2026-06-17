---
name: Eupry Design System
description: Build Eupry-branded HTML, UI, components, and emails. Use whenever creating anything visual that should look like Eupry — pages, mockups, components, newsletters, slides.
---

# Eupry Design System

You are building an **Eupry-branded** tool, page, or component. Follow these rules so the
output looks unmistakably like Eupry: clean, calm, tech-forward, generous spacing,
tight type, a near-black ink color with an icy cyan accent.

Eupry makes wireless temperature & climate monitoring for pharma, labs, and food.
The visual tone is precise and trustworthy — not playful, not corporate-grey.

## Bundled files (read these for depth)

- **`DESIGN.md`** — full spec: every color scale, type scale, component CSS, breakpoints, effects.
- **`tokens.json`** — all design tokens as structured data (richer than this file: full 50–900 color scales, z-index, transitions, component states).
- **`fonts/`** — Instrument Sans `.woff2` (8 files). Copy into the project and `@font-face` them.
- **`assets/eupry-squid.svg`** — the Eupry logo / brand mark.

Use this SKILL.md for the common case. Open `DESIGN.md` or `tokens.json` when you need a
value, scale step, or component state that isn't listed below.

---

## Non-negotiable rules

1. **Font**: Instrument Sans everywhere. `letter-spacing: -0.025em` globally.
2. **Buttons are always pill-shaped**: `border-radius: 9999px`.
3. **Headings** use `#070A26`, weight `500`. **Body text** uses `#727380`, weight `400`.
4. **Primary accent** is Brain Freeze cyan `#26DDFD`. **CTA color** is Capri Sun orange `#FF5C00`.
5. **Spacing** is a 4px scale — only use multiples of 4 (4, 8, 12, 16, 24, 32, 48, 64, 80, 96, 128).
6. **Cards** use radius `0.75rem`; **inputs** use radius `0.375rem`.
7. **Icons**: use [Lucide](https://lucide.dev) via CDN (see below). The squid mark is the only custom icon.
8. Keep it calm: lots of whitespace, thin `#EEF1F2` borders, restrained color. Don't over-decorate.

---

## Colors

### Core
| Use | Hex | Variable |
|-----|-----|----------|
| Ink / headings / dark bg | `#070A26` | `--eupry-black` |
| Body text | `#727380` | `--eupry-grey` |
| Primary accent (Brain Freeze) | `#26DDFD` | `--eupry-cyan` |
| Accent dark | `#20B3D2` | `--eupry-cyan-dark` |
| CTA (Capri Sun) | `#FF5C00` | `--eupry-orange` |
| Borders / dividers | `#EEF1F2` | `--eupry-border` |
| Light background | `#FAFBFD` | `--eupry-light-bg` |
| White | `#FFFFFF` | `--eupry-white` |

### Accent & status
| Name | Default | Dark | Light (bg tint) |
|------|---------|------|-----------------|
| Mint | `#CEFFC6` | `#A6CEA6` | `#E5F3E5` |
| Hot Pink | `#F1A7F2` | `#C288C9` | `#FCEDFB` |
| Capri Sun | `#FF5C00` | `#CD4C08` | `#FEDEDE` |
| Success | `#72BD50` | — | `#F2F8ED` |
| Warning | `#EEAA5A` | — | `#FDF7EF` |
| Error | `#EA5F5F` | — | `#FDF0EF` |

Full 50–900 scales for every color are in `tokens.json`.

---

## Typography

```css
font-family: 'Instrument Sans', sans-serif;
letter-spacing: -0.025em;
-webkit-font-smoothing: antialiased;
```

Weights: 400 regular · **500 medium (headings)** · 600 semibold · 700 bold.

| Token | px | Use |
|-------|----|----|
| xs | 13 | captions |
| sm | 14 | small text, labels |
| base | 16 | body |
| lg | 18 | lead |
| 2xl | 28 | H4 / H2 |
| 3xl | 32 | H3 |
| 4xl | 48 | H1 mobile |
| 6xl | 64 | H1 desktop |

H1 scales 48px (mobile) → 64px (desktop ≥768px), `line-height: 1`, weight 500.

### Font loading
Copy the eight `.woff2` files from `fonts/` into the project and declare them. Minimum set:

```css
@font-face { font-family:'Instrument Sans'; src:url('./fonts/InstrumentSans-Regular.woff2') format('woff2'); font-weight:400; font-display:swap; }
@font-face { font-family:'Instrument Sans'; src:url('./fonts/InstrumentSans-Medium.woff2') format('woff2'); font-weight:500; font-display:swap; }
@font-face { font-family:'Instrument Sans'; src:url('./fonts/InstrumentSans-SemiBold.woff2') format('woff2'); font-weight:600; font-display:swap; }
@font-face { font-family:'Instrument Sans'; src:url('./fonts/InstrumentSans-Bold.woff2') format('woff2'); font-weight:700; font-display:swap; }
```

---

## Logo

The Eupry logo is the **squid** mark (in `assets/eupry-squid.svg`), usually paired with the
lowercase "eupry" wordmark.

```html
<a href="https://eupry.com" class="logo">
  <svg class="logo-icon" width="24" height="24" viewBox="0 0 24 24" fill="none">
    <path d="M7.71429 12C7.71429 14.6036 5.60363 16.7143 3 16.7143L3 21C7.96584 21 11.9923 16.9782 12 12.0141C12.0076 16.9782 16.0341 21 21 21L21 16.7143C18.3963 16.7143 16.2857 14.6036 16.2857 12L7.71429 12Z" fill="#070A26"/>
    <path d="M16.7143 12C16.7143 9.39639 14.6036 7.28573 12 7.28573C9.39638 7.28574 7.28573 9.39636 7.28573 12L3.00002 12C3.00002 7.02943 7.02946 3 12 3C16.9706 3.00001 21 7.02946 21 12H16.7143Z" fill="#070A26"/>
  </svg>
  <span class="logo-text">eupry</span>
</a>
```
```css
.logo { display:flex; align-items:center; gap:0.5rem; }
.logo-icon { width:24px; height:24px; }
.logo-text { font-size:1.25rem; font-weight:600; color:#070A26; letter-spacing:-0.03em; }
/* On dark backgrounds: set both path fills and .logo-text color to #FFFFFF */
```

---

## Icons — Lucide via CDN

```html
<!-- once, before </body> -->
<script src="https://unpkg.com/lucide@latest"></script>
<script>lucide.createIcons();</script>

<!-- anywhere -->
<i data-lucide="thermometer"></i>
<i data-lucide="bell-ring"></i>
```
```css
[data-lucide] { width:20px; height:20px; stroke-width:2; color:currentColor; }
```
Names are kebab-case; confirm at https://lucide.dev/icons. Never invent names — pick the
closest real Lucide icon. Common: `arrow-right`, `chevron-down`, `check`, `x`, `search`,
`menu`, `thermometer`, `droplet`, `snowflake`, `wifi`, `battery`, `bell`, `triangle-alert`,
`circle-check`, `map-pin`, `house`, `user`, `settings`, `external-link`.

---

## Components

### Button (pill)
```css
.btn { display:inline-flex; align-items:center; justify-content:center; gap:0.5rem;
  font-family:'Instrument Sans',sans-serif; font-weight:500; border:none;
  border-radius:9999px; cursor:pointer; transition:all 300ms ease; }
.btn-default { padding:0.875rem 1.25rem; font-size:1rem; }
.btn-small   { padding:0.5rem 1.25rem; font-size:0.875rem; }
.btn-primary { background:#070A26; color:#fff; }      /* default action */
.btn-cta     { background:#FF5C00; color:#fff; }      /* primary CTA */
.btn-accent  { background:#26DDFD; color:#070A26; }   /* highlight */
.btn-outline { background:transparent; color:#070A26; border:1px solid #070A26; }
```

### Card
```css
.card { background:#fff; border:1px solid #EEF1F2; border-radius:0.75rem; overflow:hidden; }
.card-image { width:100%; height:13rem; object-fit:cover; }
.card-body { padding:1.5rem; }
.card-title { font-size:1rem; font-weight:500; color:#070A26; margin-bottom:0.5rem; }
.card-text { font-size:0.875rem; color:#727380; }
```

### Input
```css
input, textarea, select {
  width:100%; padding:0.75rem 1rem; font-family:'Instrument Sans',sans-serif;
  font-size:1rem; color:#070A26; background:#fff;
  border:1px solid #CDCED4; border-radius:0.375rem;
  transition:border-color 200ms ease, box-shadow 200ms ease; }
input::placeholder { color:#9C9DA7; }
input:focus { outline:none; border-color:#26DDFD; box-shadow:0 0 0 2px rgba(38,221,253,0.2); }
input.error { border-color:#EA5F5F; }
input:disabled { background:#F3F3F4; color:#9C9DA7; cursor:not-allowed; }
```

### Glass header
```css
.header { position:sticky; top:0; z-index:30;
  background:rgba(255,255,255,0.8); backdrop-filter:blur(8px);
  -webkit-backdrop-filter:blur(8px); border-bottom:1px solid #EEF1F2; }
```

### Container
```css
.container { width:100%; max-width:1280px; margin-inline:auto; padding-inline:1rem; }
@media (min-width:640px){ .container { padding-inline:2rem; } }
```

---

## CSS variables (paste into `:root`)

```css
:root{
  --eupry-black:#070A26; --eupry-cyan:#26DDFD; --eupry-cyan-dark:#20B3D2;
  --eupry-grey:#727380; --eupry-border:#EEF1F2; --eupry-light-bg:#FAFBFD; --eupry-white:#FFFFFF;
  --eupry-orange:#FF5C00; --eupry-mint:#CEFFC6; --eupry-pink:#F1A7F2;
  --eupry-success:#72BD50; --eupry-warning:#EEAA5A; --eupry-error:#EA5F5F;
}
```

---

## When generating a full page, always

- Set `box-sizing:border-box`, reset margins, apply the body font + `letter-spacing:-0.025em` + `color:#727380`.
- Use the glass header with the logo top-left.
- Constrain content to `.container` (max 1280px).
- Give sections generous vertical padding (≥ 4rem).
- Use `#FAFBFD` for alternating section backgrounds, `#EEF1F2` for hairline dividers.
- Pill buttons; cyan for highlights, orange for the single primary CTA.
- Lucide icons via CDN; the squid logo for branding.
