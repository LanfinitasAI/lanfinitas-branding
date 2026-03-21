# lanfinitas-branding

Official brand assets, design tokens, and web fonts for Lanfinitas AI / CircuLab.

---

## What's in this repo

```text
lanfinitas-branding/
├── fonts/
│   ├── RamaGothicC-*.woff2
│   ├── RamaGothicE-*.woff2
│   ├── RamaGothicM-*.woff2
│   ├── SpaceMono-*.woff2
│   └── stylesheet.css
├── design-tokens.md
└── README.md
```

| File | Purpose |
|------|---------|
| `fonts/stylesheet.css` | Web font entry point — embed in any HTML |
| `design-tokens.md` | Full colour system, typography scale, component patterns |

---

## Font Usage

```html
<link rel="stylesheet" href="https://lanfinitasai.github.io/lanfinitas-branding/fonts/stylesheet.css">
```

Then apply the brand font stack:

```css
font-family: 'Rama Gothic E', 'Rama Gothic M', 'Space Mono', system-ui, sans-serif;
```

---

## Design Tokens

See [`design-tokens.md`](./design-tokens.md) for the full specification.

Quick reference — CSS variables:

```css
:root {
  /* Backgrounds */
  --bg-void:      #000000;   /* pure black */
  --bg-base:      #0d0d0d;   /* main app background */
  --bg-surface:   #1a1a1a;   /* panels, sidebars, cards */
  --bg-raised:    #242424;   /* inputs, hover states */
  --bg-overlay:   #2e2e2e;   /* tooltips, dropdowns */

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

## Usage with Claude Skills and Agents

Claude Skills can emit HTML that includes both the font stylesheet and token definitions:

```html
<link rel="stylesheet" href="https://lanfinitasai.github.io/lanfinitas-branding/fonts/stylesheet.css">
```

This ensures consistent typography and colour across all web-based outputs — internal tools, static sites, PDF pipelines, and agent-generated documents.

---

## Hosted URLs (GitHub Pages)

| Asset | URL |
|-------|-----|
| Font stylesheet | `https://lanfinitasai.github.io/lanfinitas-branding/fonts/stylesheet.css` |
| Design tokens | `https://lanfinitasai.github.io/lanfinitas-branding/design-tokens.md` |

---

## Note on repo rename

This repository was previously named `lanfinitas-fonts`. It has been expanded to cover the full Lanfinitas brand system including design tokens, colour scale, and typography rules. GitHub automatically redirects old URLs for 12 months — update any hardcoded references to use the new path.

---

## License

Assets in this repository are provided solely for Lanfinitas AI / CircuLab branded materials and approved collaborators. Request permission before using outside the Lanfinitas ecosystem.

*Lanfinitas AI · lanfinitasai.com · © 2026 All rights reserved*
