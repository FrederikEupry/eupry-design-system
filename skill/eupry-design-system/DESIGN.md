# Eupry Design System

**Version**: 2.0 | **Last Updated**: 2026-06-17

This document serves as the design backbone for creating Eupry-branded tools and applications.

---

## Table of Contents

1. [Brand Colors](#1-brand-colors)
2. [Typography](#2-typography)
3. [Spacing & Layout](#3-spacing--layout)
4. [Border & Radius](#4-border--radius)
5. [Shadows & Effects](#5-shadows--effects)
6. [Buttons](#6-buttons)
7. [Form Elements](#7-form-elements)
8. [Cards](#8-cards)
9. [Icons](#9-icons)
10. [Responsive Breakpoints](#10-responsive-breakpoints)
11. [CSS Variables](#11-css-variables)
12. [Quick Reference](#12-quick-reference)
13. [Usage in External Tools](#usage-in-external-tools)
14. [Folder Structure](#folder-structure)

---

## 1. Brand Colors

### Primary Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Eupry Black** | `#070A26` | rgb(7, 10, 38) | Primary dark, text, backgrounds |
| **Brain Freeze Blue** | `#26DDFD` | rgb(38, 221, 253) | Primary accent, CTAs, highlights |
| **White** | `#FFFFFF` | rgb(255, 255, 255) | Backgrounds, text on dark |

### Eupry Black Scale

| Step | Hex | Usage |
|------|-----|-------|
| DEFAULT | `#070A26` | Primary brand black |
| 900 | `#20233B` | |
| 800 | `#393B50` | |
| 700 | `#515466` | |
| 600 | `#6A6C7C` | |
| 500 | `#838491` | |
| 400 | `#9C9DA7` | Placeholder text |
| 300 | `#B5B5BD` | |
| 200 | `#CDCED4` | Input borders |
| 100 | `#E6E6E9` | |
| 50 | `#F3F3F4` | Subtle backgrounds |

### Brain Freeze Blue Scale (Primary Accent)

| Step | Hex | Usage |
|------|-----|-------|
| Dark | `#20B3D2` | Darker variant for contrast |
| DEFAULT | `#26DDFD` | Primary cyan accent |
| 900 | `#4ADFFA` | |
| 800 | `#5BE3FB` | |
| 700 | `#6EE6FC` | |
| 600 | `#83EAFC` | |
| 500 | `#92EEFE` | |
| 400 | `#ABF0FD` | |
| 300 | `#C0F5FD` | |
| 200 | `#D5F8FE` | Light background tint |
| 100 | `#EAFCFF` | |
| 50 | `#F4FDFF` | Subtle highlight |

### Secondary Accent Colors

#### Mint Green
| Variant | Hex | Usage |
|---------|-----|-------|
| Dark | `#A6CEA6` | Text on light, darker UI |
| DEFAULT | `#CEFFC6` | Success states, highlights |
| Light | `#E5F3E5` | Background tints |

#### Hot Pink
| Variant | Hex | Usage |
|---------|-----|-------|
| Dark | `#C288C9` | Text on light, darker UI |
| DEFAULT | `#F1A7F2` | Accent, special highlights |
| Light | `#FCEDFB` | Background tints |

#### Capri Sun (Orange)
| Variant | Hex | Usage |
|---------|-----|-------|
| Dark | `#CD4C08` | Text on light, darker UI |
| DEFAULT | `#FF5C00` | CTAs, action items, warnings |
| Light | `#FEDEDE` | Background tints |

### Status Colors

| Status | Default | Light (for backgrounds) |
|--------|---------|-------------------------|
| **Success** | `#72BD50` | `#F2F8ED` |
| **Warning/Progress** | `#EEAA5A` | `#FDF7EF` |
| **Error** | `#EA5F5F` | `#FDF0EF` |

### Utility Colors

| Name | Hex | Usage |
|------|-----|-------|
| Dark Grey | `#727380` | Body text, secondary text |
| Grey | `#EEF1F2` | Borders, dividers |
| Light Grey | `#FAFBFD` | Subtle backgrounds |

---

## 2. Typography

### Font Family

**Primary Font**: Instrument Sans

```css
font-family: 'Instrument Sans', sans-serif;
```

**Available Weights**:
- Regular (400)
- Medium (500) - **Primary for headings**
- Semi-Bold (600)
- Bold (700)

**Font Loading** (for web projects):
```css
@font-face {
  font-family: 'Instrument Sans';
  src: url('./fonts/InstrumentSans-Regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Instrument Sans';
  src: url('./fonts/InstrumentSans-Medium.woff2') format('woff2');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Instrument Sans';
  src: url('./fonts/InstrumentSans-SemiBold.woff2') format('woff2');
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Instrument Sans';
  src: url('./fonts/InstrumentSans-Bold.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}
```

### Type Scale

| Name | Size | Line Height | Pixels | Usage |
|------|------|-------------|--------|-------|
| `xxs` | 0.6875rem | 1rem | 11px | Fine print, labels |
| `xs` | 0.8125rem | 1.3125rem | 13px | Captions, metadata |
| `sm` | 0.875rem | 1.25rem | 14px | Small text |
| `base` | 1rem | 1.5rem | 16px | Body text |
| `lg` | 1.125rem | 1.75rem | 18px | Lead paragraphs |
| `xl` | 1.3125rem | 2rem | 21px | Large body |
| `2xl` | 1.75rem | 2rem | 28px | H4, small headings |
| `3xl` | 2rem | 2rem | 32px | H3 |
| `3.5xl` | 2.5rem | 3rem | 40px | H2 |
| `4xl` | 3rem | 3.5rem | 48px | H1 (mobile) |
| `5xl` | 3.5rem | 3.75rem | 56px | H1 (tablet) |
| `6xl` | 4rem | 4rem | 64px | H1 (desktop hero) |

### Heading Styles

```css
/* H1 - Hero/Page Title */
h1 {
  font-size: 3rem;        /* Mobile: 48px (4xl) */
  font-weight: 500;
  line-height: 1;
  letter-spacing: -0.025em;
  color: #070A26;
}
@media (min-width: 768px) {
  h1 { font-size: 4rem; } /* Desktop: 64px (6xl) */
}

/* H2 - Section Title */
h2 {
  font-size: 1.75rem;     /* 28px (2xl) */
  font-weight: 500;
  line-height: 1;
  color: #070A26;
}

/* H3 - Subsection */
h3 {
  font-size: 2rem;        /* 32px (3xl) */
  font-weight: 500;
  color: #070A26;
}

/* H4-H6 */
h4, h5, h6 {
  font-weight: 500;
  color: #070A26;
}
```

### Body Text

```css
body {
  font-family: 'Instrument Sans', sans-serif;
  font-size: 1rem;
  line-height: 1.5;
  letter-spacing: -0.025em;  /* tracking-tight */
  color: #727380;            /* dark-grey */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

/* Links */
a {
  color: #070A26;
  text-decoration: none;
}
a:hover {
  color: #727380;
}

/* Lead/Intro Text */
.lead {
  font-size: 1.125rem;
  color: #727380;
}
```

---

## 3. Spacing & Layout

### Spacing Scale

| Class | Value | Pixels | Common Usage |
|-------|-------|--------|--------------|
| `1` | 0.25rem | 4px | Tight gaps |
| `2` | 0.5rem | 8px | Icon gaps, small padding |
| `3` | 0.75rem | 12px | Button padding |
| `4` | 1rem | 16px | Default padding |
| `5` | 1.25rem | 20px | - |
| `6` | 1.5rem | 24px | Card padding, gaps |
| `8` | 2rem | 32px | Section gaps |
| `10` | 2.5rem | 40px | - |
| `12` | 3rem | 48px | Large spacing |
| `14` | 3.5rem | 56px | Hero spacing |
| `16` | 4rem | 64px | Section padding |
| `20` | 5rem | 80px | Major sections |
| `24` | 6rem | 96px | Large sections |
| `32` | 8rem | 128px | Hero margins |

### Container

```css
.container {
  width: 100%;
  max-width: 1280px;
  margin-left: auto;
  margin-right: auto;
  padding-left: 1rem;
  padding-right: 1rem;
}

@media (min-width: 640px) {
  .container {
    padding-left: 2rem;
    padding-right: 2rem;
  }
}
```

### Common Layout Patterns

```css
/* Section Spacing */
section {
  padding-top: 4rem;    /* py-16 */
  padding-bottom: 4rem;
}

/* Grid - 3 columns */
.grid-3 {
  display: grid;
  gap: 1.5rem;
  grid-template-columns: 1fr;
}
@media (min-width: 768px) {
  .grid-3 {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* Grid - 2 columns */
.grid-2 {
  display: grid;
  gap: 2rem;
  grid-template-columns: 1fr;
}
@media (min-width: 768px) {
  .grid-2 {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

---

## 4. Border & Radius

### Border Radius Scale

| Name | Value | Pixels | Usage |
|------|-------|--------|-------|
| `sm` | 0.125rem | 2px | Subtle rounding |
| `DEFAULT` | 0.25rem | 4px | Default |
| `md` | 0.375rem | 6px | Inputs, small cards |
| `lg` | 0.5rem | 8px | Dropdowns, menus |
| `xl` | 0.75rem | 12px | Cards |
| `2xl` | 1rem | 16px | Large cards, videos |
| `3xl` | 1.5rem | 24px | - |
| `4xl` | 2rem | 32px | Large containers |
| `full` | 9999px | - | Pills, buttons, avatars |

### Common Border Patterns

```css
/* Default border */
border: 1px solid #EEF1F2;

/* Input border */
border: 1px solid #CDCED4;

/* Focus ring */
outline: 2px solid #26DDFD;
outline-offset: 2px;

/* Card border */
border: 1px solid #EEF1F2;
border-radius: 0.75rem;
```

---

## 5. Shadows & Effects

### Box Shadows

```css
/* Drop shadow - buttons, cards */
box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1),
            0 1px 2px -1px rgb(0 0 0 / 0.1);

/* Elevated shadow - dropdowns, modals */
box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1),
            0 4px 6px -4px rgb(0 0 0 / 0.1);

/* Large shadow - hero images */
box-shadow: 0 25px 50px -12px rgb(0 0 0 / 0.25);
```

### Glass Morphism (Header)

```css
.glass {
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}
```

### Transitions

```css
/* Color transitions */
transition: color 300ms ease;

/* Transform transitions */
transition: transform 300ms ease;

/* Menu animations */
transition: all 500ms ease;

/* Hover arrow animation */
transition: transform 700ms ease;
transform: translateX(0.25rem); /* on hover */
```

---

## 6. Buttons

### Button Variants

| Variant | Background | Text | Border |
|---------|------------|------|--------|
| **Primary (Black)** | `#070A26` | `#FFFFFF` | none |
| **Secondary (White)** | `#FFFFFF` | `#070A26` | none |
| **Outline** | transparent | `#070A26` | `1px solid #070A26` |
| **Brain Freeze** | `#26DDFD` | `#070A26` | none |
| **Brain Freeze Dark** | `#20B3D2` | `#FFFFFF` | none |
| **Capri Sun** | `#FF5C00` | `#FFFFFF` | none |
| **Capri Sun Dark** | `#CD4C08` | `#FFFFFF` | none |
| **Mint Green** | `#CEFFC6` | `#070A26` | none |
| **Mint Green Dark** | `#A6CEA6` | `#FFFFFF` | none |
| **Hot Pink** | `#F1A7F2` | `#070A26` | none |
| **Hot Pink Dark** | `#C288C9` | `#FFFFFF` | none |

### Button Sizes

| Size | Padding | Font Size |
|------|---------|-----------|
| Small | `0.5rem 1.25rem` (py-2 px-5) | 14px |
| Default | `0.875rem 1.25rem` (py-3.5 px-5) | 16px |
| Login | `0.5rem 1rem` (py-2 px-4) | 14px |

### Button CSS

```css
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  font-family: 'Instrument Sans', sans-serif;
  font-weight: 500;
  border-radius: 9999px;
  cursor: pointer;
  transition: all 300ms ease;
}

.btn-default {
  padding: 0.875rem 1.25rem;
  font-size: 1rem;
}

.btn-small {
  padding: 0.5rem 1.25rem;
  font-size: 0.875rem;
}

/* Primary */
.btn-primary {
  background-color: #070A26;
  color: #FFFFFF;
  box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1);
}

/* Secondary */
.btn-secondary {
  background-color: #FFFFFF;
  color: #070A26;
  box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1);
}

/* Outline */
.btn-outline {
  background-color: transparent;
  color: #070A26;
  border: 1px solid #070A26;
}

/* With arrow icon */
.btn .arrow {
  transition: transform 700ms ease;
}
.btn:hover .arrow {
  transform: translateX(0.25rem);
}
```

---

## 7. Form Elements

### Input Fields

```css
input[type="text"],
input[type="email"],
input[type="password"],
input[type="tel"],
textarea,
select {
  width: 100%;
  padding: 0.75rem 1rem;
  font-family: 'Instrument Sans', sans-serif;
  font-size: 1rem;
  color: #070A26;
  background-color: #FFFFFF;
  border: 1px solid #CDCED4;
  border-radius: 0.375rem;
  transition: border-color 200ms ease, box-shadow 200ms ease;
}

input::placeholder,
textarea::placeholder {
  color: #9C9DA7;
}

input:focus,
textarea:focus,
select:focus {
  outline: none;
  border-color: #26DDFD;
  box-shadow: 0 0 0 2px rgba(38, 221, 253, 0.2);
}

/* Error state */
input.error {
  border-color: #EA5F5F;
}

/* Disabled state */
input:disabled {
  background-color: #F3F3F4;
  color: #9C9DA7;
  cursor: not-allowed;
}
```

### Labels

```css
label {
  display: block;
  margin-bottom: 0.5rem;
  font-size: 0.875rem;
  font-weight: 500;
  color: #070A26;
}
```

### Checkboxes & Radios

```css
input[type="checkbox"],
input[type="radio"] {
  width: 1.25rem;
  height: 1.25rem;
  accent-color: #26DDFD;
}
```

---

## 8. Cards

### Basic Card

```css
.card {
  background-color: #FFFFFF;
  border: 1px solid #EEF1F2;
  border-radius: 0.75rem;
  overflow: hidden;
}

.card-image {
  width: 100%;
  height: 13rem; /* h-52 = 208px */
  object-fit: cover;
}

.card-body {
  padding: 1.5rem;
}

.card-title {
  font-size: 1rem;
  font-weight: 500;
  color: #070A26;
  margin-bottom: 0.5rem;
}

.card-text {
  font-size: 0.875rem;
  color: #727380;
}
```

### Card Grid

```css
.card-grid {
  display: grid;
  gap: 1.5rem;
  grid-template-columns: 1fr;
}

@media (min-width: 768px) {
  .card-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

---

## 9. Icons

### Icon Library

Use [**Lucide**](https://lucide.dev) for all UI icons. The only custom Eupry icon is the `eupry-squid` logo/brand mark (see Logo section) — everything else comes from Lucide. Browse and confirm exact names at https://lucide.dev/icons. Names are kebab-case (e.g. `arrow-right`, `thermometer`, `bell-ring`, `triangle-alert`). Never invent icon names; if one doesn't exist, pick the closest real Lucide icon.

**Delivery: CDN.** Add the script once, then use `data-lucide` attributes:

```html
<!-- once, before </body> -->
<script src="https://unpkg.com/lucide@latest"></script>
<script>lucide.createIcons();</script>

<!-- anywhere -->
<i data-lucide="thermometer"></i>
<i data-lucide="bell-ring"></i>
```

Or fetch a single SVG directly (no script): `https://unpkg.com/lucide-static@latest/icons/{name}.svg`

### Icon Sizing

| Size | Pixels | Usage |
|------|--------|-------|
| `xs` | 12px | Inline, badges |
| `sm` | 16px | Buttons, labels |
| `md` | 20px | Default |
| `lg` | 24px | Navigation |
| `xl` | 32px | Feature icons |
| `2xl` | 48px | Hero icons |

### Icon Colors

- Default: `currentColor` (inherits text color)
- Interactive: Changes with hover state
- Accent: Use brand colors for emphasis

### Common Icons (Lucide names)

**Navigation**: `arrow-right`, `arrow-left`, `arrow-up`, `arrow-down`, `chevron-up`, `chevron-down`, `chevron-left`, `chevron-right`, `house`, `map-pin`

**Actions**: `check`, `x`, `download`, `pencil`, `search`, `plus`, `minus`, `trash-2`, `settings`

**Status**: `circle-check`, `circle-x`, `bell`, `info`, `triangle-alert`, `shield-check`

**Temperature/Monitoring**: `thermometer`, `droplet`, `snowflake`, `wifi`, `battery`, `cloud`

**UI**: `menu`, `ellipsis`, `external-link`

### Using Icons

```html
<!-- once, before </body> -->
<script src="https://unpkg.com/lucide@latest"></script>
<script>lucide.createIcons();</script>

<!-- anywhere -->
<i data-lucide="arrow-right"></i>
```

```css
/* Icon styling — Lucide is stroke-based and inherits currentColor */
[data-lucide], .icon {
  width: 1.25rem;
  height: 1.25rem;
  stroke-width: 2;
  color: currentColor;
}
```

---

## 10. Responsive Breakpoints

| Name | Min Width | Target |
|------|-----------|--------|
| `sm` | 640px | Large phones |
| `md` | 768px | Tablets |
| `lg` | 1024px | Small laptops |
| `xl` | 1280px | Desktops |
| `2xl` | 1280px | Large desktops |

### Media Query Usage

```css
/* Mobile first approach */
.element {
  /* Mobile styles (default) */
  padding: 1rem;
}

@media (min-width: 640px) {
  .element {
    /* sm: Large phones */
    padding: 1.5rem;
  }
}

@media (min-width: 768px) {
  .element {
    /* md: Tablets */
    padding: 2rem;
  }
}

@media (min-width: 1024px) {
  .element {
    /* lg: Laptops */
    padding: 2.5rem;
  }
}

@media (min-width: 1280px) {
  .element {
    /* xl: Desktops */
    padding: 3rem;
  }
}
```

---

## 11. CSS Variables

Copy these CSS custom properties for easy theming:

```css
:root {
  /* Brand Colors */
  --color-black: #070A26;
  --color-black-900: #20233B;
  --color-black-800: #393B50;
  --color-black-700: #515466;
  --color-black-600: #6A6C7C;
  --color-black-500: #838491;
  --color-black-400: #9C9DA7;
  --color-black-300: #B5B5BD;
  --color-black-200: #CDCED4;
  --color-black-100: #E6E6E9;
  --color-black-50: #F3F3F4;

  /* Primary Accent - Brain Freeze Blue */
  --color-primary: #26DDFD;
  --color-primary-dark: #20B3D2;
  --color-primary-light: #D5F8FE;
  --color-primary-50: #F4FDFF;

  /* Secondary - Mint Green */
  --color-mint: #CEFFC6;
  --color-mint-dark: #A6CEA6;
  --color-mint-light: #E5F3E5;

  /* Secondary - Hot Pink */
  --color-pink: #F1A7F2;
  --color-pink-dark: #C288C9;
  --color-pink-light: #FAE5FA;

  /* Secondary - Capri Sun (Orange) */
  --color-orange: #FF5C00;
  --color-orange-dark: #CD4C08;
  --color-orange-light: #FEDECE;

  /* Status */
  --color-success: #72BD50;
  --color-success-light: #F2F8ED;
  --color-warning: #EEAA5A;
  --color-warning-light: #FDF7EF;
  --color-error: #EA5F5F;
  --color-error-light: #FDF0EF;

  /* Utility */
  --color-grey: #EEF1F2;
  --color-grey-dark: #727380;
  --color-grey-light: #FAFBFD;
  --color-white: #FFFFFF;

  /* Typography */
  --font-family: 'Instrument Sans', sans-serif;
  --font-size-base: 1rem;
  --line-height-base: 1.5;
  --letter-spacing: -0.025em;

  /* Spacing */
  --spacing-1: 0.25rem;
  --spacing-2: 0.5rem;
  --spacing-3: 0.75rem;
  --spacing-4: 1rem;
  --spacing-6: 1.5rem;
  --spacing-8: 2rem;
  --spacing-12: 3rem;
  --spacing-16: 4rem;

  /* Border Radius */
  --radius-sm: 0.125rem;
  --radius-md: 0.375rem;
  --radius-lg: 0.5rem;
  --radius-xl: 0.75rem;
  --radius-2xl: 1rem;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  --shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);

  /* Container */
  --container-max: 1280px;
  --container-padding: 1rem;
}

@media (min-width: 640px) {
  :root {
    --container-padding: 2rem;
  }
}
```

---

## 12. Quick Reference

### Essential Colors

| Use Case | Color | Hex |
|----------|-------|-----|
| Primary text | Eupry Black | `#070A26` |
| Body text | Dark Grey | `#727380` |
| Primary accent | Brain Freeze | `#26DDFD` |
| CTA buttons | Capri Sun | `#FF5C00` |
| Success | Green | `#72BD50` |
| Error | Red | `#EA5F5F` |
| Borders | Grey | `#EEF1F2` |
| Background | White | `#FFFFFF` |

### Essential Typography

```css
/* Base setup */
font-family: 'Instrument Sans', sans-serif;
letter-spacing: -0.025em;
-webkit-font-smoothing: antialiased;

/* Headings: font-weight: 500 */
/* Body: color: #727380 */
/* Links: color: #070A26 */
```

### Essential Components

```css
/* Button */
border-radius: 9999px;
padding: 0.875rem 1.25rem;
font-weight: 500;

/* Card */
border: 1px solid #EEF1F2;
border-radius: 0.75rem;
padding: 1.5rem;

/* Input */
border: 1px solid #CDCED4;
border-radius: 0.375rem;
padding: 0.75rem 1rem;
```

### Logo & Favicon

- **Favicon**: 48x48px circle with Eupry symbol
- **Logo**: Eupry wordmark + symbol
- **Colors**: `#070A26` on white, white on `#070A26`

### Font Files

Located at: `./fonts/` (woff2 format only)
- InstrumentSans-Regular.woff2
- InstrumentSans-Medium.woff2
- InstrumentSans-SemiBold.woff2
- InstrumentSans-Bold.woff2

### Icons

Use [Lucide](https://lucide.dev) via CDN (see Section 9). The `eupry-squid` brand mark is the only custom icon.

---

## Usage in External Tools

When creating external Eupry-branded tools:

1. **Include the font** - Copy font files from `./fonts/` folder
2. **Include icons** - Use Lucide via CDN (see Section 9)
3. **Copy CSS variables** - Use the variables from Section 11
4. **Match the color scheme** - Primary black + Brain Freeze accent
5. **Use rounded buttons** - `border-radius: 9999px` for pills
6. **Keep spacing generous** - Minimum 1rem (16px) padding
7. **Maintain typography** - Medium weight for headings, tight tracking

### Minimal CSS Starter

```css
/* Add the @font-face rules from Section 2 (Typography) here, or inline them */

:root {
  --eupry-black: #070A26;
  --eupry-cyan: #26DDFD;
  --eupry-grey: #727380;
  --eupry-border: #EEF1F2;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Instrument Sans', sans-serif;
  color: var(--eupry-grey);
  letter-spacing: -0.025em;
  -webkit-font-smoothing: antialiased;
}

h1, h2, h3, h4, h5, h6 {
  color: var(--eupry-black);
  font-weight: 500;
}

a {
  color: var(--eupry-black);
  text-decoration: none;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.875rem 1.25rem;
  font-weight: 500;
  border-radius: 9999px;
  border: none;
  cursor: pointer;
}

.btn-primary {
  background: var(--eupry-black);
  color: white;
}

.btn-accent {
  background: var(--eupry-cyan);
  color: var(--eupry-black);
}
```

---

## Folder Structure

```
DESIGN SYSTEM/
├── DESIGN.md          # This file
└── fonts/             # Instrument Sans font files (.woff2 only)
    ├── InstrumentSans-Regular.woff2
    ├── InstrumentSans-Medium.woff2
    ├── InstrumentSans-SemiBold.woff2
    └── InstrumentSans-Bold.woff2
```

---

**Source**: Extracted from the Eupry website codebase (`tailwind.config.js`, CSS, and Vue components).
