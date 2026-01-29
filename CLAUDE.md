# Eupry Design System - Agent Reference

Quick reference for AI agents. For full details, see `DESIGN.md`. For structured data, see `tokens.json`.

## Files

```
eupry-design-system/
├── CLAUDE.md          # This file (quick reference)
├── DESIGN.md          # Full documentation
├── icon-index.json    # Icon lookup (categories, aliases) - USE THIS FIRST
├── tokens.json        # Design tokens as structured data
├── icons/             # Individual SVG files (208 icons)
└── fonts/             # Instrument Sans (.woff2)
```

## Logo

**The `eupry-squid` icon is the main Eupry logo/brand mark.** Use it for headers and branding.

```html
<!-- Standard logo: icon + text -->
<a href="https://eupry.com" class="logo">
  <svg class="logo-icon" width="24" height="24" viewBox="0 0 24 24" fill="none">
    <path d="M7.71429 12C7.71429 14.6036 5.60363 16.7143 3 16.7143L3 21C7.96584 21 11.9923 16.9782 12 12.0141C12.0076 16.9782 16.0341 21 21 21L21 16.7143C18.3963 16.7143 16.2857 14.6036 16.2857 12L7.71429 12Z" fill="#070A26"/>
    <path d="M16.7143 12C16.7143 9.39639 14.6036 7.28573 12 7.28573C9.39638 7.28574 7.28573 9.39636 7.28573 12L3.00002 12C3.00002 7.02943 7.02946 3 12 3C16.9706 3.00001 21 7.02946 21 12H16.7143Z" fill="#070A26"/>
  </svg>
  <span class="logo-text">eupry</span>
</a>
```

```css
.logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.logo-icon { width: 24px; height: 24px; }
.logo-text {
  font-size: 1.25rem;
  font-weight: 600;
  color: #070A26;
  letter-spacing: -0.03em;
}
```

| Variant | Icon fill | Text color | Usage |
|---------|-----------|------------|-------|
| Default | `#070A26` | `#070A26` | Light backgrounds |
| Inverted | `#FFFFFF` | `#FFFFFF` | Dark backgrounds |

## Icon Lookup

**Always check `icon-index.json` first** - it has categories and aliases.

```javascript
// Find icon by category
categories.navigation  // arrows, chevrons, home, map-pin
categories.actions     // checkmark, cross, plus, minus, edit, search
categories.status      // bell, alarm, info, shield, deviation
categories.communication // chat, email, phone, headset
categories.files       // document, folder, archive, book
categories.temperature // therometer, humidity, snowflake, fridge

// Find icon by alias
aliases.menu       → "burgermenu"
aliases.close      → "cross"
aliases.check      → "checkmark"
aliases.delete     → "trash"
aliases.settings   → "settings"
aliases.user       → "user1"

// Get SVG: read ./icons/{icon-name}.svg
```

## Colors

### Brand
| Name | Hex | Usage |
|------|-----|-------|
| Eupry Black | `#070A26` | Primary text, dark bg |
| Brain Freeze | `#26DDFD` | Primary accent |
| Brain Freeze Dark | `#20B3D2` | Darker cyan variant |
| White | `#FFFFFF` | Backgrounds |

### Text & UI
| Name | Hex | Usage |
|------|-----|-------|
| Dark Grey | `#727380` | Body text |
| Grey | `#EEF1F2` | Borders, dividers |
| Light Grey | `#FAFBFD` | Light backgrounds |
| Black 400 | `#9C9DA7` | Placeholder text |

### Accent Colors
| Name | Default | Dark | Light |
|------|---------|------|-------|
| Capri Sun | `#FF5C00` | `#CD4C08` | `#FEDEDE` |
| Mint | `#CEFFC6` | `#A6CEA6` | `#E5F3E5` |
| Hot Pink | `#F1A7F2` | `#C288C9` | `#FCEDFB` |

### Status
| Status | Default | Light bg |
|--------|---------|----------|
| Success | `#72BD50` | `#F2F8ED` |
| Warning | `#EEAA5A` | `#FDF7EF` |
| Error | `#EA5F5F` | `#FDF0EF` |

### Testimonial Colors (text on colored bg)
- Green bg `#CEFFC6` → text `#375834`
- Blue bg `#D5F8FE` → text `#0F4853`
- Orange bg `#FEDECE` → text `#4E1F05`

## Typography

```css
font-family: 'Instrument Sans', sans-serif;
letter-spacing: -0.025em;  /* tracking-tight */
```

| Size | rem | px | Usage |
|------|-----|----|----|
| xxs | 0.6875 | 11 | Labels, badges |
| xs | 0.8125 | 13 | Captions |
| sm | 0.875 | 14 | Small text |
| base | 1 | 16 | Body |
| lg | 1.125 | 18 | Lead text |
| xl | 1.3125 | 21 | Large body |
| 2xl | 1.75 | 28 | H4 |
| 3xl | 2 | 32 | H3 |
| 3.5xl | 2.5 | 40 | H2 |
| 4xl | 3 | 48 | H1 mobile |
| 5xl | 3.5 | 56 | H1 tablet |
| 6xl | 4 | 64 | H1 desktop |

**Weights**: 400 (regular), 500 (medium - headings), 600 (semibold), 700 (bold)

## Components

### Button
```css
border-radius: 9999px;      /* pill shape */
font-weight: 500;
/* Default */ padding: 0.875rem 1.25rem;
/* Small */   padding: 0.5rem 1.25rem;
/* Login */   padding: 0.5rem 1rem;
```

| Variant | Background | Text |
|---------|------------|------|
| Primary | `#070A26` | white |
| Secondary | `#FFFFFF` | black |
| Outline | transparent | black + border |
| Brain Freeze | `#26DDFD` | black |
| Brain Freeze Dark | `#20B3D2` | white |
| Capri Sun | `#FF5C00` | white |
| Capri Sun Dark | `#CD4C08` | white |
| Mint | `#CEFFC6` | black |
| Hot Pink | `#F1A7F2` | black |

### Card
```css
border: 1px solid #EEF1F2;
border-radius: 0.75rem;     /* rounded-xl */
padding: 1.5rem;
/* Image height: 13rem (h-52) */
```

### Input
```css
border: 1px solid #CDCED4;
border-radius: 0.375rem;    /* rounded-md */
padding: 0.75rem 1rem;
/* Focus: border-color: #26DDFD; box-shadow: 0 0 0 2px rgba(38, 221, 253, 0.2) */
/* Error: border-color: #EA5F5F */
/* Disabled: bg: #F3F3F4, color: #9C9DA7 */
```

### Input (Dark background)
```css
background: rgba(255, 255, 255, 0.2);
border: 1px solid rgba(255, 255, 255, 0.2);
color: #FFFFFF;
/* Focus ring: white */
```

### Dropdown
```css
min-width: 200px;
border-radius: 0.5rem;      /* rounded-lg */
padding: 0.75rem 0;
box-shadow: /* shadow-lg */;
/* Item padding: 0.5rem 1.5rem */
```

### Badge
```css
padding: 0.5rem;
border-radius: 0.25rem;
font-size: 11px;            /* text-xxs */
text-transform: uppercase;
```

### Header (Glass)
```css
background: rgba(255, 255, 255, 0.8);
backdrop-filter: blur(8px);
border-bottom: 1px solid #EEF1F2;
/* Logo height: 22px */
```

## Spacing Scale

| Key | Value | px |
|-----|-------|----|
| 0.5 | 0.125rem | 2 |
| 1 | 0.25rem | 4 |
| 2 | 0.5rem | 8 |
| 3 | 0.75rem | 12 |
| 4 | 1rem | 16 |
| 6 | 1.5rem | 24 |
| 8 | 2rem | 32 |
| 12 | 3rem | 48 |
| 16 | 4rem | 64 |
| 20 | 5rem | 80 |
| 24 | 6rem | 96 |
| 32 | 8rem | 128 |

## Border Radius

| Name | Value | Usage |
|------|-------|-------|
| sm | 0.125rem | Subtle |
| md | 0.375rem | Inputs |
| lg | 0.5rem | Dropdowns |
| xl | 0.75rem | Cards |
| 2xl | 1rem | Large cards |
| 4xl | 2rem | Sections |
| full | 9999px | Buttons, pills |

## Breakpoints

| Name | Width | Container padding |
|------|-------|-------------------|
| sm | 640px | 1rem |
| md | 768px | 2rem |
| lg | 1024px | 2rem |
| xl | 1280px | 2rem |

**Container max-width**: 1280px

## Transitions

| Speed | Duration | Usage |
|-------|----------|-------|
| fast | 200ms | Quick feedback |
| default | 300ms | Standard |
| medium | 500ms | Menus, dropdowns |
| slow | 700ms | Arrow animations |

**Easing**: `ease` (default), `cubic-bezier(0.33, 1, 0.68, 1)` (collapse/expand)

## Effects

### Glass Morphism
```css
background: rgba(255, 255, 255, 0.8);
backdrop-filter: blur(8px);
```

### Gradients
```css
/* Fade to black (top) */
background: linear-gradient(to bottom, #000, transparent);

/* Horizontal divider */
background: linear-gradient(to right, transparent, #EEF1F2, transparent);
```

### Shadows
```css
/* sm */  0 1px 2px 0 rgb(0 0 0 / 0.05)
/* md */  0 4px 6px -1px rgb(0 0 0 / 0.1)
/* lg */  0 10px 15px -3px rgb(0 0 0 / 0.1)
/* xl */  0 25px 50px -12px rgb(0 0 0 / 0.25)
/* drop */ drop-shadow(0px 20px 20px rgba(0, 0, 0, 0.1))
```

## Z-Index Scale

| Name | Value | Usage |
|------|-------|-------|
| base | 0 | Default |
| content | 10 | Above content |
| overlay | 20 | Overlays |
| header | 30 | Fixed header |
| modal | 40 | Modals |
| tooltip | 50 | Tooltips |

## Hover States

```css
/* Text */ hover:text-dark-grey
/* Opacity */ hover:opacity-90
/* Scale */ hover:scale-105
/* Background */ hover:bg-grey, hover:bg-black/5
/* Arrow */ group-hover:translate-x-1 (with transition-transform duration-700)
```

## CSS Variables Snippet

```css
:root {
  /* Brand */
  --eupry-black: #070A26;
  --eupry-cyan: #26DDFD;
  --eupry-cyan-dark: #20B3D2;

  /* Text */
  --eupry-grey: #727380;
  --eupry-border: #EEF1F2;
  --eupry-light-bg: #FAFBFD;

  /* Accent */
  --eupry-orange: #FF5C00;
  --eupry-mint: #CEFFC6;
  --eupry-pink: #F1A7F2;

  /* Status */
  --eupry-success: #72BD50;
  --eupry-warning: #EEAA5A;
  --eupry-error: #EA5F5F;
}
```
