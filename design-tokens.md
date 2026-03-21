# Lanfinitas Design Tokens
**Version:** 1.0  
**Established:** March 2026  
**Status:** Production — SpecFlow TVP0

---

## Colour System

Lanfinitas uses a pure black foundation with a structured grey scale for legibility. The system has two poles — `#000000` and `#ffffff` — with seven intermediate values that govern all UI surfaces, text, and borders.

### Background Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--bg-void` | `#000000` | Pure black — logo backgrounds, hard borders only |
| `--bg-base` | `#0d0d0d` | Main application background |
| `--bg-surface` | `#1a1a1a` | Panels, sidebars, cards, modals |
| `--bg-raised` | `#242424` | Input fields, hover states, account panel |
| `--bg-overlay` | `#2e2e2e` | Tooltips, dropdowns, active toggle states |

### Text Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--text-primary` | `#f0f0f0` | Headings, style numbers, active values |
| `--text-secondary` | `#b0b0b0` | Body text, descriptions, field values, labels |
| `--text-tertiary` | `#6e6e6e` | Placeholders, disabled states, section labels |
| `--text-ghost` | `#3a3a3a` | Decorative text, watermarks, coming-soon items |

### Border Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--border-strong` | `#3a3a3a` | Input borders, card borders, sidebar edges |
| `--border-subtle` | `#242424` | Section separators, divider lines |

### Accent

| Token | Value | Usage |
|-------|-------|-------|
| `--accent-white` | `#ffffff` | Primary buttons, logo, active headings |
| `--accent-red` | `#cc0000` | Error states, danger zone, credit exhausted bar |

---

## CSS Implementation

Copy this block into any HTML file's `<style>` tag or external stylesheet:

```css
:root {
  /* Backgrounds */
  --bg-void:      #000000;
  --bg-base:      #0d0d0d;
  --bg-surface:   #1a1a1a;
  --bg-raised:    #242424;
  --bg-overlay:   #2e2e2e;

  /* Text */
  --text-primary:   #f0f0f0;
  --text-secondary: #b0b0b0;
  --text-tertiary:  #6e6e6e;
  --text-ghost:     #3a3a3a;

  /* Borders */
  --border-strong:  #3a3a3a;
  --border-subtle:  #242424;

  /* Accents */
  --accent-white:  #ffffff;
  --accent-red:    #cc0000;
}
```

---

## Typography

### Font Stack (priority order)

**English:**
1. Rama Gothic E
2. Rama Gothic M
3. Space Mono
4. System monospace fallback

**Chinese:**
1. 黑体 / Heiti
2. Noto Sans CJK / Source Han Sans
3. PingFang SC
4. System sans-serif fallback

### Font Loading

```html
<link rel="stylesheet" href="https://lanfinitasai.github.io/lanfinitas-fonts/fonts/stylesheet.css">
```

### Size & Weight

| Role | Size | Weight |
|------|------|--------|
| Display heading | 48–96px | 700–900 |
| Section heading | 18–24px | 500–700 |
| Body text | 13–15px | 400 |
| Label / tag | 10–12px | 500, letter-spacing 0.08em |
| Monospace value | 13–14px | 400 (Space Mono) |

---

## Component Patterns

### Input Field
```css
background: var(--bg-raised);
border: 1px solid var(--border-strong);
color: var(--text-primary);
/* placeholder */ color: var(--text-tertiary);
```

### Card / Panel
```css
background: var(--bg-surface);
border: 1px solid var(--border-strong);
border-radius: 2px; /* Lanfinitas uses minimal rounding */
```

### Primary Button (white)
```css
background: #ffffff;
color: #000000;
border: none;
```

### Secondary Button (outline)
```css
background: transparent;
color: var(--text-primary);
border: 1px solid var(--border-strong);
```

### Section Label
```css
color: var(--text-tertiary);
font-size: 10px;
font-weight: 500;
letter-spacing: 0.1em;
text-transform: uppercase;
```

### Sidebar / Panel Edge
```css
background: var(--bg-surface);
border-left: 1px solid var(--border-strong);
```

---

## Colour Usage Rules

1. **Never use pure black (`#000`) as text** — use `--text-primary` (`#f0f0f0`) on dark backgrounds
2. **Never place `--text-tertiary` on `--bg-void`** — minimum pairing is tertiary on surface
3. **White (`#ffffff`) is reserved for primary actions and the logo** — do not use for body text
4. **Red (`--accent-red`) is for destructive/error states only** — never decorative
5. **All interactive elements must have a visible border** — minimum `--border-subtle` at rest, `--border-strong` on hover/focus
6. **Sidebar backgrounds must differ from main background** — use `--bg-surface` for panels against `--bg-base` body

---

## Two-Colour Document Mode

For exported documents (PDF tech packs, letters, presentations):

| Mode | Background | Text |
|------|-----------|------|
| Dark (default) | `#000000` | `#ffffff` |
| Light | `#ffffff` | `#000000` |

Document exports do not use the grey scale — pure black/white only.

---

## Hosted Reference

Fonts stylesheet:  
`https://lanfinitasai.github.io/lanfinitas-fonts/fonts/stylesheet.css`

This tokens file (once published):  
`https://lanfinitasai.github.io/lanfinitas-branding/design-tokens.md`

---

*Lanfinitas AI · lanfinitasai.com · © 2026 All rights reserved*
