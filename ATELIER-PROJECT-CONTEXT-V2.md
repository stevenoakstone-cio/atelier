# ATELIER — Complete Project Context for v2.0
## Drop this file in the project root. Claude Code reads this + the prompt to build v2.0.

**Last Updated:** February 4, 2026
**Project:** Single-page "Living Brand Book" website for ATELIER pastry brand
**Client:** Cristina
**Location:** Monterrey, MX
**Style:** European Bistro / Japandi / Silent Luxury
**Live URL:** https://stevenoakstone-cio.github.io/atelier/
**Repository:** https://github.com/stevenoakstone-cio/atelier.git
**Local Path:** `C:\Users\EdgeAdmin\Documents\Claude_Projects_2026\bakery-cristina`

---

## 1. CURRENT STATE — WHAT EXISTS

### Live URLs
| URL | Description |
|-----|-------------|
| https://stevenoakstone-cio.github.io/atelier/ | Main site (copy of index1.3.html) |
| https://stevenoakstone-cio.github.io/atelier/index-v1-original.html | V1: Japandi neutral palette |
| https://stevenoakstone-cio.github.io/atelier/index-v2-warm.html | V2: Warm Mediterranean palette |
| https://stevenoakstone-cio.github.io/atelier/index-v3-cool.html | V3: Cool French luxury palette |

### Website (v1.3 — Currently Live)
- 10-section scrollytelling single-page website
- Sections: Hero, Esencia de Marca, Valores (4 flip cards), Personalidad, Tono de Voz, Identidad Visual, Paleta de Colores (click-to-copy HEX+CMYK), Tipografía, Fotografía, Footer
- Loading screen with pulsing logo
- Hero parallax scrolling effect
- Scroll animations (Intersection Observer)
- Hover-reveal value cards with centered text
- Click-to-copy color palette (HEX + CMYK)
- Sticky navigation with dot indicators
- Open Graph meta tags + og-image.png for social sharing
- Mobile-responsive, prefers-reduced-motion accessibility
- Built with vanilla HTML/CSS/JS, Google Fonts (Playfair Display + Montserrat)

### 3 Color Variations (Built & Deployed)
- V1 Original (Japandi): Crema #F2F0E9 · Carbón #333333 · Terracota #C78D76 · Salvia #A4B0A0
- V2 Warm (Mediterranean): Crema Cálida #FDF8F3 · Chocolate #3D2C29 · Terracota Intenso #C46E4E · Caramelo #D4A574
- V3 Cool (French): Gris Perla #F5F5F5 · Azul Noche #1A1A2E · Bronce #8B7355 · Azul Acero #6B7B8C
- **Status:** Waiting for Cristina to choose her palette.

### Brand Guidelines Document
`ATELIER-Brand-Guidelines.md` — Complete brand manual with Misión/Visión/Valores, brand personality archetype, tone of voice, logo rules, color specs (HEX/RGB/CMYK), typography hierarchy, photography style guide, content pillars, and application recommendations.

---

## 2. FILE STRUCTURE (Current + New Assets)

```
bakery-cristina/
├── index.html                        # Main file on GitHub Pages (copy of v1.3)
├── index1.2.html                     # Older version
├── index1.3.html                     # Latest development version (BASE FOR v2.0)
├── index-v1-original.html            # V1 Japandi palette
├── index-v2-warm.html                # V2 Warm palette
├── index-v3-cool.html                # V3 Cool palette
├── og-image.html                     # Canvas tool to generate social sharing PNG
├── og-image.png                      # Social sharing image (1200x630px)
│
├── logo-bakery.svg                   # Combined logo — flower + text fused (#4d4c4d)
├── logo-bakery-white.svg             # Combined logo — white (#FFFFFF)
├── logo-bakery-dark.svg              # Combined logo — charcoal (#333333)
├── logo-bakery-terracotta.svg        # Combined logo — terracotta (#C78D76)
├── isotype_logo.svg                  # ★ NEW — Flower only, separate (#4c4b4b)
├── isotype_logo.png                  # ★ NEW — Flower raster reference
├── name_logo.svg                     # ★ NEW — Wordmark "ATELIER" only (#494948)
├── name_logo.png                     # ★ NEW — Wordmark raster reference
│
├── ATELIER-Brand-Guidelines.md       # Complete brand manual
├── ATELIER-PROJECT-HANDOFF.md        # Original handoff document
├── ATELIER-PROJECT-CONTEXT-V2.md     # ★ THIS FILE
├── atelier-3-variations.md           # 3 color palette instructions
├── bakery-cristina-instructions.md   # Original build instructions
└── PROJECT-CONTEXT.md                # Earlier project documentation
```

---

## 3. LOGO SYSTEM — COMPLETE INVENTORY

We now have **3 separate logo components** as clean SVGs:

### 3.1 Combined Logo (`logo-bakery.svg`)
- Flower + "ATELIER" text fused into one flattened auto-trace
- Original fill: `#4d4c4d`
- 4 color variations already exist as separate files (white, dark, terracotta)
- Source: Google Flow → vectorized

### 3.2 Isotype — Flower Symbol (`isotype_logo.svg`) ★ NEW
- Flower only, cleanly separated
- viewBox: `0 0 1563 893`
- Single `<path>` element, fill: `#4c4b4b`
- File size: ~2KB — lightweight, easy to embed and recolor
- Source: Separated from original via Google Flow + vectorized

### 3.3 Wordmark (`name_logo.svg`) ★ NEW
- "ATELIER" text only, cleanly separated
- viewBox: `0 0 1344 768`
- Multiple `<path>` elements (one per letter group), fill: `#494948`
- File size: ~4KB
- Source: Separated from original via Google Flow + vectorized

### 3.4 Color Variations Needed (Generate in v2.0 via inline SVG fill swap)

| Variation | HEX | Use case |
|-----------|-----|----------|
| Original (dark gray) | #4c4b4b / #4d4c4d | Light backgrounds |
| White | #FFFFFF | Dark backgrounds, footer |
| Charcoal | #333333 | Brand-consistent dark |
| Terracotta | #C78D76 | Accent / special applications |
| Sage | #A4B0A0 | Secondary accent |

Apply all 5 to each of the 3 logo types = 15 inline variants total.

### 3.5 Asset Status

| Asset | Status | Source File |
|-------|--------|-------------|
| Combined logo (flower + text) | ✅ Done | `logo-bakery.svg` + 3 color variants |
| Isotype (flower only) | ✅ Done | `isotype_logo.svg` |
| Wordmark (text only) | ✅ Done | `name_logo.svg` |
| Combined logo color variants (4) | ✅ Done | white, dark, terracotta SVG files |
| Isotype color variants (5) | 🔄 v2.0 | Inline SVG fill swap |
| Wordmark color variants (5) | 🔄 v2.0 | Inline SVG fill swap |
| Favicon | 🔄 v2.0 | Generate from isotype |
| Badge / secondary logo | ❌ Phase 2 | Flower inside circle shape |
| Brand pattern / texture | 🔄 v2.0 | CSS geometric + isotype watermark |

### 3.6 PNGs Note
`isotype_logo.png` and `name_logo.png` are JPEG-encoded files with `.png` extension, black backgrounds (not transparent). They are reference copies only — use the SVGs for everything.

---

## 4. DESIGN SYSTEM

### Colors (CSS Variables)
```css
:root {
    --color-bone: #F2F0E9;        /* Primary background */
    --color-charcoal: #333333;    /* Primary text */
    --color-terracotta: #C78D76;  /* Accent, CTAs, highlights */
    --color-sage: #A4B0A0;        /* Secondary backgrounds */
}
```

### Full Color Specifications
| Color | Name | HEX | RGB | CMYK |
|-------|------|-----|-----|------|
| Background | Crema Hueso | #F2F0E9 | 242, 240, 233 | 0, 1, 4, 5 |
| Text | Carbón Suave | #333333 | 51, 51, 51 | 0, 0, 0, 80 |
| Accent | Terracota | #C78D76 | 199, 141, 118 | 0, 29, 41, 22 |
| Secondary | Salvia | #A4B0A0 | 164, 176, 160 | 7, 0, 9, 31 |

### Typography
- **Playfair Display** (400, 700) — Headings, titles
- **Montserrat** (300, 400, 500) — Body text, navigation, buttons

---

## 5. CLIENT FEEDBACK — WHY v2.0 IS NEEDED

Cristina reviewed v1.3 and said: **"It looks nice but it feels incomplete."**

### What She's Missing:
1. **Isotype & Graphic Variants** — She wants to see the flower symbol alone, badge versions, brand patterns → ★ NOW RESOLVED with isotype_logo.svg
2. **Downloadable Files** — She expects a hub where she can download AI, EPS, PNG, Canva templates
3. **Social Media Guide** — Specific guidance for Instagram/Facebook posting
4. **Packaging Mockups** — More visual applications
5. **Overall: She wants a "Client Portal" not just a "Mood Board"**

---

## 6. v2.0 TARGET — SECTION ORDER

Use `index1.3.html` as the base. Output: `index-v2.0.html`

```
1.  Hero ("Bienvenida, Cristina" + isotype + wordmark stacked)  ← UPDATED
2.  Esencia de Marca (Misión / Visión)
3.  Nuestros Valores (4 flip cards)
4.  Personalidad ("El Creador Intimista")
5.  Tono de Voz (Do's / Don'ts)
6.  Identidad Visual (Logo showcase)
7.  Normativa Técnica (Clear space, incorrect uses)              ← NEW
8.  Versatilidad de Marca (Logo on 3 backgrounds)               ← NEW
9.  Sistema Gráfico (Architecture, variants, patterns)           ← NEW
10. Paleta de Colores (Click-to-copy)
11. Tipografía (Font hierarchy)
12. Fotografía (Style guide)
13. Redes Sociales y Presencia Digital (IG mockup, strategy)     ← NEW
14. Zona de Cliente (Download hub)                               ← NEW
15. Próximos Pasos (Roadmap timeline)                            ← NEW
16. Footer (CTAs, version, approval button)                      ← UPDATED
```

---

## 7. v2.0 SECTION DETAILS

### 7.1 Hero UPDATE
- Add kicker: "Bienvenida, Cristina. Esta es la visión de tu marca." (small uppercase Montserrat, 0.3em letter-spacing, fade-in)
- Use **isotype** (flower) small and centered above the **wordmark** (`name_logo.svg`) — stacked vertically, replaces the combined logo

### 7.2 Loading Screen UPDATE
- Replace combined logo with **isotype** (flower)
- Animate: fade in + scale from 0.8→1.0, then fade out to reveal page

### 7.3 Normativa Técnica (Section 7 — NEW)
- **Clear Space (Área de Seguridad):** Combined logo with dashed border, measurement unit = height of "A"
- **Minimum Sizes:** Digital 40px · Print 1.5cm · Serigrafía 2cm
- **Incorrect Uses (2×2 grid):** 4 "don'ts" using CSS transforms on the combined logo:
  1. "No Distorsionar" → `scaleX(1.5)`
  2. "No Rotar" → `rotate(15deg)`
  3. "No Bajo Contraste" → `opacity: 0.2`
  4. "No Cambiar Colores" → non-brand fill (e.g., `#2196F3`)
- Each gets a red diagonal strike-through (CSS pseudo-element) + label

### 7.4 Versatilidad de Marca (Section 8 — NEW)
- 3-column grid (stacks mobile):
  1. Bone `#F2F0E9` bg → dark combined logo → "Packaging / Papelería"
  2. Terracotta `#C78D76` bg → white combined logo → "Stickers / Acentos"
  3. Sage `#A4B0A0` bg → white combined logo → "Corporativo"

### 7.5 Sistema Gráfico (Section 9 — NEW, COMPLETE)
**9a. Arquitectura de Marca (3-column):**
  1. **Isotipo** — flower from `isotype_logo.svg` → "Uso independiente en favicon, stickers, marcas de agua"
  2. **Logotipo** — wordmark from `name_logo.svg` → "Uso en papelería formal, headers"
  3. **Logo Completo** — combined from `logo-bakery.svg` → "Uso principal en todas las aplicaciones"

**9b. Variantes de Color:**
  Toggle/tab interface: switch between Isotipo / Logotipo / Logo Completo, showing 5 color variants each (original, white-on-dark, charcoal, terracotta, sage). HEX label + use-case subtitle under each.

**9c. Brand Pattern Strip:**
  - CSS geometric pattern (thin lines/dots in terracotta/sage on bone), ~80px tall
  - Secondary variant: isotype tiled at very low opacity (0.05–0.08) as watermark
  - Show both side by side

### 7.6 Redes Sociales y Presencia Digital (Section 13 — NEW)
- **Instagram Phone Mockup:** CSS phone frame with 3×3 grid:
  - 3 Unsplash bakery images + 6 brand-colored placeholders (some with isotype watermark)
- **Posting Strategy:** Frecuencia 3–4/semana · Horarios 10am/2pm/7pm · Hashtags · Pilares (40/25/20/15 stacked bar chart in CSS)
- **Caption Examples:** ✅ good vs ❌ bad
- **Download CTA:** "Descargar Estrategia Social Media (PDF)" → `href="#"`

### 7.7 Zona de Cliente (Section 14 — NEW, MOST IMPORTANT)
Dashboard-style download hub. 6 cards (3 cols desktop, 2 tablet, 1 mobile):

| Card | Format | Description | Status |
|------|--------|-------------|--------|
| Master Vectors | .AI / .EPS | Logos editables para imprenta | 🔒 Fase 2 |
| Kit Digital | .PNG / .SVG | Logos para redes y presentaciones | ✅ Disponible |
| Manual de Marca | .PDF | Manual de uso y estrategia | ✅ Disponible |
| Pack Social Media | .PSD / Canva | Plantillas editables para posts | 🔒 Fase 2 |
| Kit de Fotografía | .PDF | Guía de estilo fotográfico | 🔒 Fase 2 |
| Papelería | .AI / .PDF | Tarjetas, membrete, facturas | 🔒 Fase 2 |

- "Disponible" = active hover, download icon, `href="#"`
- "Fase 2" = lock icon, muted, "Próximamente" label

### 7.8 Próximos Pasos (Section 15 — NEW)
Horizontal timeline (vertical on mobile):
- **Fase 1 ✅** Identidad Visual · Manual de Marca · Portal Web · Isotipo
- **Fase 2 🔄** Papelería · Templates Social Media · Badge Logo
- **Fase 3 📋** Packaging · Mockups · Material Impreso

### 7.9 Footer UPDATE
- Dark bg with white **isotype** stacked above white **wordmark** (replaces combined logo)
- Two CTAs: "Descargar Kit de Marca" (outline) + "Aprobar esta dirección" (terracotta filled, mailto)
- Version: "Manual v2.0 — Febrero 2026"
- Text: "ATELIER. Est. 2026. Monterrey, MX."

### 7.10 Favicon
- Generate from isotype SVG
- Inline as `<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,...">` with charcoal fill

### 7.11 Dot Navigation
- Update to 16 sections with abbreviated Spanish hover labels

---

## 8. CURATED UNSPLASH IMAGES

| Use | URL |
|-----|-----|
| Hero texture | `https://images.unsplash.com/photo-1558961363-fa8fdf82db35?q=80&w=2065` |
| Origin / hands | `https://images.unsplash.com/photo-1507048331197-7d4febed500e?q=80&w=1500` |
| Product 1 | `https://images.unsplash.com/photo-1626265774643-f1943311a86b` |
| Product 2 | `https://images.unsplash.com/photo-1595928607828-4c3114ba5a22` |
| Product 3 | `https://images.unsplash.com/photo-1516919549054-e08258825f80` |

---

## 9. BRAND CONTENT (Spanish — Reference)

### Misión
Crear repostería artesanal de precisión, donde cada detalle refleja amor por el proceso y respeto por el oficio. No buscamos producción masiva, sino perfección individual.

### Visión
Ser reconocidos como el taller de repostería de referencia en Monterrey — sinónimo de perfección silenciosa, belleza comestible y experiencias memorables.

### Valores
1. **Calidad Radical** — Si no es perfecto, no sale del taller. Preferimos no vender a vender algo a medias.
2. **Estética Silenciosa** — El amor entra por los ojos. El montaje es nuestra firma de autor.
3. **Honestidad** — Prometemos solo lo que podemos cumplir. Transparencia absoluta en ingredientes y procesos.
4. **El Proceso es Sagrado** — La limpieza y el orden no se negocian. La repostería es disciplina y respeto.

### Arquetipo: El Creador Intimista
Somos como esa anfitriona impecable que habla en voz baja, pero todos callan para escucharla. No gritamos para vender. Somos elegantes, sofisticados, pero con un guiño de calidez humana.

### Tono de Voz
✅ "Dicen que la perfección no existe, pero tal vez no han probado nuestro equilibrio de texturas. Un pequeño capricho para su martes. (O miércoles, nadie lleva la cuenta)."
❌ "¡¡Los mejores postres de MTY!! 🎂🔥 PIDE YA con 20% de descuento!!!"

### Origin Story
Lo que nació observando a mi madre hacer su mostachón, se convirtió en mi refugio. Encontré en la repostería la paz que da la precisión. No es solo cocinar; es un momento de conexión. Hoy, ATELIER es la evolución de esa herencia: perfeccionismo técnico con alma artesanal.

---

## 10. KNOWN ISSUES & SOLUTIONS

| Issue | Solution |
|-------|----------|
| Value card text at top, not centered | Made `.card-front`/`.card-back` position: absolute with justify-content: center |
| Section numbers barely visible | Increased font-size to 0.85rem, weight 500, charcoal with 0.7 opacity |
| SVG doesn't show in social previews | Created PNG via og-image.html — social platforms require raster images |
| Windows `copy` command fails in bash | Use `cp` instead |
| Logo was flattened SVG | ★ RESOLVED — isotype and wordmark now separated |
| Standalone HTML breaks with external SVGs | Embed SVGs inline for v2.0 |
| PNGs are JPEG-encoded with black bg | Use SVGs only — PNGs are reference copies |

---

## 11. DEPLOYMENT WORKFLOW

```bash
cd "C:\Users\EdgeAdmin\Documents\Claude_Projects_2026\bakery-cristina"

# After Claude Code creates index-v2.0.html:
cp index-v2.0.html index.html

# Push to GitHub
git add .
git commit -m "v2.0 - Client portal with full logo system and download hub"
git push

# Live at: https://stevenoakstone-cio.github.io/atelier/
```

### GitHub Pages Settings
- Source: Deploy from branch
- Branch: main
- Folder: / (root)

---

## 12. PENDING TASKS (Priority Order)

### 🔴 HIGH — Do Now
1. [ ] Copy `isotype_logo.svg` and `name_logo.svg` into project root
2. [ ] Run the v2.0 Claude Code prompt with this context file
3. [ ] Review `index-v2.0.html` locally
4. [ ] Push to GitHub and test live

### 🟡 MEDIUM — This Week
5. [ ] Get Cristina's color palette choice (V1/V2/V3)
6. [ ] Create badge version (flower inside circle) — Recraft or Figma
7. [ ] Create actual downloadable files for Zona de Cliente (PDF brand manual, PNG kit ZIP)
8. [ ] Generate transparent PNGs of isotype + wordmark (replace black-bg ones)

### 🟢 LOW — Phase 2
9. [ ] Design social media templates in Canva
10. [ ] Create stationery (business cards, thank-you cards, stickers)
11. [ ] Packaging mockups (Figma/Lumière template)
12. [ ] Print stylesheet for brand manual
13. [ ] Apple touch icon from isotype (180×180)

---

*This file supersedes PROJECT-CONTEXT.md and ATELIER-PROJECT-HANDOFF.md*
*Version: v2.0 pre-build context*
