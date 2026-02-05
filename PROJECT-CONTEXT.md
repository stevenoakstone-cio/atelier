# ATELIER Brand Manual Website — Project Context

**Project:** Single-page brand manual website for ATELIER pastry brand
**Location:** Monterrey, MX
**Style:** European Bistro / Japandi / Silent Luxury
**Live URL:** https://stevenoakstone-cio.github.io/atelier/
**Repository:** https://github.com/stevenoakstone-cio/atelier.git

---

## 1. Project Overview

A scrollytelling single-page website showcasing the complete brand guidelines for ATELIER, a premium artisanal pastry brand. The site features:

- 9 sections covering brand essence, values, personality, tone of voice, visual identity, photography, and applications
- Interactive scroll animations using Intersection Observer API
- Hover-reveal value cards with centered text
- Click-to-copy color palette (HEX + CMYK values)
- Sticky navigation with dot indicators
- Loading screen animation with pulsing logo
- Hero parallax scrolling effect
- Social sharing with Open Graph meta tags
- Responsive design with mobile optimizations
- Prefers-reduced-motion accessibility support

---

## 2. File Structure

```
bakery-cristina/
├── index.html                    # Main file for GitHub Pages (copy of index1.3.html)
├── index1.2.html                 # Earlier version
├── index1.3.html                 # Latest development version
├── og-image.html                 # Canvas tool to generate social sharing PNG
├── og-image.png                  # Social sharing image (1200x630px)
├── logo-bakery.svg               # Main logo (gray #4d4c4d) - nav & visual identity
├── logo-bakery-white.svg         # White logo - footer (dark background)
├── logo-bakery-dark.svg          # Dark logo (#333333)
├── logo-bakery-terracotta.svg    # Terracotta logo (#C78D76)
├── ATELIER-Brand-Guidelines.md   # Source brand guidelines document
├── bakery-cristina-instructions.md # Original build instructions
└── PROJECT-CONTEXT.md            # This file
```

---

## 3. Design System

### Colors (CSS Variables)
```css
--color-bone: #F2F0E9;        /* Primary background */
--color-charcoal: #333333;    /* Primary text */
--color-terracotta: #C78D76;  /* Accent, CTAs, highlights */
--color-sage: #A4B0A0;        /* Secondary backgrounds, subtle elements */
```

### Typography (Google Fonts)
- **Playfair Display** (400, 700) — Headings, titles
- **Montserrat** (300, 400, 500) — Body text, navigation, buttons

### CMYK Values (for print)
| Color | HEX | CMYK |
|-------|-----|------|
| Crema Hueso | #F2F0E9 | 0, 1, 4, 5 |
| Carbón Suave | #333333 | 0, 0, 0, 80 |
| Terracota | #C78D76 | 0, 29, 41, 22 |
| Salvia | #A4B0A0 | 7, 0, 9, 31 |

---

## 4. Key Features Implemented

### 4.1 Loading Screen
- Pulsing logo animation
- Fades out after fonts load
- Uses CSS keyframes for pulse effect

### 4.2 Scroll Animations
- Elements fade in and slide up on scroll
- Uses Intersection Observer API with 0.1 threshold
- Respects `prefers-reduced-motion` for accessibility

### 4.3 Value Cards (Hover-Reveal)
- Front shows value name (centered)
- Back reveals full description on hover
- 3D flip effect with `transform: rotateY(180deg)`
- Both sides use `position: absolute` with `justify-content: center`

### 4.4 Color Palette
- Click any color card to copy HEX code
- Shows both HEX and CMYK values
- Visual feedback on copy with checkmark

### 4.5 Hero Parallax
- Background moves at 50% scroll speed on desktop
- Disabled on mobile for performance
- Uses `transform: translateY()` for smooth animation

### 4.6 Navigation
- Sticky header with blur backdrop
- Dot indicators show current section
- Smooth scroll to sections on click

### 4.7 Social Sharing (Open Graph)
```html
<meta property="og:title" content="ATELIER — Manual de Marca">
<meta property="og:description" content="Repostería de Detalle. Manual de identidad visual y lineamientos de marca.">
<meta property="og:image" content="https://stevenoakstone-cio.github.io/atelier/og-image.png">
<meta property="og:url" content="https://stevenoakstone-cio.github.io/atelier/">
<meta property="og:type" content="website">
<meta name="twitter:card" content="summary_large_image">
```

---

## 5. Website Sections

1. **Hero** — Full-screen with logo and tagline
2. **Esencia de Marca** — Mission, vision, brand essence
3. **Nuestros Valores** — 4 interactive hover-reveal cards
4. **Personalidad** — Brand archetype and keywords
5. **Tono de Voz** — Communication style with examples
6. **Identidad Visual** — Logo usage and specifications
7. **Paleta de Colores** — Click-to-copy color cards
8. **Tipografía** — Font hierarchy and examples
9. **Fotografía** — Visual style guidelines
10. **Footer** — Contact info with white logo on dark background

---

## 6. Deployment Steps

### Initial Setup (already done)
```bash
cd "C:\Users\EdgeAdmin\Documents\Claude_Projects_2026\bakery-cristina"
git init
git remote add origin https://github.com/stevenoakstone-cio/atelier.git
```

### Push Updates
```bash
git add <filename>
git commit -m "Description of changes"
git push
```

### Files Pushed to GitHub
- index.html (main page)
- logo-bakery.svg
- logo-bakery-white.svg
- logo-bakery-dark.svg
- logo-bakery-terracotta.svg
- og-image.png

### GitHub Pages Settings
- Source: Deploy from branch
- Branch: main
- Folder: / (root)

---

## 7. OG Image Generator

The `og-image.html` file creates a 1200x630px PNG for social sharing:

1. Open `og-image.html` in a browser
2. Wait for fonts to load (canvas renders automatically)
3. Click "Descargar og-image.png"
4. Push the downloaded PNG to GitHub

The image includes:
- Bone background (#F2F0E9)
- ATELIER logo (or text fallback)
- "Manual de Marca" title
- "REPOSTERÍA DE DETALLE" subtitle
- Decorative corner accents

---

## 8. Known Issues & Solutions

| Issue | Solution |
|-------|----------|
| Value card text at top, not centered | Made `.card-front` and `.card-back` position: absolute with justify-content: center |
| Section numbers barely visible | Increased font-size to 0.85rem, weight 500, charcoal color with 0.7 opacity, terracotta number highlight |
| SVG doesn't show in social previews | Created PNG generator (og-image.html) - social platforms require raster images |
| Windows `copy` command fails in bash | Use `cp` instead |

---

## 9. Future Improvements (Optional)

### Quick Wins
- [x] Loading animation
- [x] Hero parallax effect
- [x] CMYK values in color palette

### Medium Effort
- [ ] Scroll progress indicator bar at top
- [ ] Dark mode toggle
- [ ] Downloadable PDF version of brand manual
- [ ] Print stylesheet

### Advanced
- [ ] Multi-language support (ES/EN)
- [ ] CMS integration for easy updates
- [ ] Animation on logo in hero (subtle movement)

---

## 10. Brand Guidelines Summary

### Mission
Crear repostería artesanal de precisión, donde cada detalle refleja amor por el proceso y respeto por el oficio.

### Vision
Ser reconocidos como el taller de repostería de referencia en Monterrey — sinónimo de perfección silenciosa, belleza comestible y experiencias memorables.

### Core Values
1. **Calidad Radical** — Si no es perfecto, no sale del taller
2. **Estética Silenciosa** — El amor entra por los ojos
3. **Honestidad** — Prometemos solo lo que podemos cumplir
4. **El Proceso es Sagrado** — La limpieza y el orden no se negocian

### Brand Archetype
**El Creador Intimista** — Elegantes, sofisticados, pero con un guiño de calidez humana

### Keywords
Precisión, Silencio, Elegancia, Artesanal, Detalle, Calidez, Japandi, Lujo silencioso

---

## 11. Contact & Credits

**ATELIER**
Repostería de Detalle
Monterrey, MX
Est. 2026

---

*Document created: February 2026*
*Last updated: February 4, 2026*
