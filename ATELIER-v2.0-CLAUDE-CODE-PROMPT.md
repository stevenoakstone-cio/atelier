# ATELIER v2.0 — Claude Code Build Prompt (Updated)

> Paste this entire prompt into Claude Code from inside the project directory:
> `C:\Users\EdgeAdmin\Documents\Claude_Projects_2026\bakery-cristina`
>
> **Before running:** Make sure these files exist in the project root:
> - `logo-bakery.svg` (combined logo — flower + text fused)
> - `logo-bakery-white.svg`, `logo-bakery-dark.svg`, `logo-bakery-terracotta.svg`
> - `isotype_logo.svg` (flower only — NEW)
> - `name_logo.svg` (wordmark "ATELIER" only — NEW)
> - `isotype_logo.png`, `name_logo.png` (raster references)

---

## PROMPT START — COPY FROM HERE ↓

Read the file `ATELIER-PROJECT-HANDOFF.md` in this directory for full project context, brand content, and design system details. That document is the single source of truth.

Use `index1.3.html` as the base template. Create `index-v2.0.html` — a single standalone HTML file with ALL CSS and JS inline.

---

### LOGO ASSETS — READ THIS FIRST

We now have **3 separate logo components** as clean SVGs. Read each file and embed them inline:

**1. Combined Logo** (`logo-bakery.svg`) — Flower + "ATELIER" text fused together
- Original fill: `#4d4c4d`
- Existing color variations: `logo-bakery-white.svg` (#FFFFFF), `logo-bakery-dark.svg` (#333333), `logo-bakery-terracotta.svg` (#C78D76)

**2. Isotype / Flower Symbol** (`isotype_logo.svg`) — Flower only, separate
- viewBox: `0 0 1563 893`
- Original fill: `#4c4b4b`
- Single `<path>` element — lightweight, easy to recolor

**3. Wordmark** (`name_logo.svg`) — "ATELIER" text only, separate
- viewBox: `0 0 1344 768`
- Original fill: `#494948`
- Multiple `<path>` elements (one per letter group)

**For inline embedding:** Read the raw SVG content of each file and embed the `<svg>` markup directly in the HTML. Do NOT use `<img src="...">`. When you need a color variation, duplicate the inline SVG and change the `fill` attribute on all paths.

**Generate these color variations inline (for all 3 logo types):**

| Variation | HEX | CSS class suffix | Use case |
|-----------|-----|-----------------|----------|
| Original (dark gray) | #4c4b4b / #4d4c4d | `-original` | Light backgrounds |
| White | #FFFFFF | `-white` | Dark backgrounds, footer |
| Charcoal | #333333 | `-dark` | Brand-consistent dark |
| Terracotta | #C78D76 | `-terracotta` | Accent / special |
| Sage | #A4B0A0 | `-sage` | Secondary accent |

Create the color variants by swapping the `fill` value on the SVG paths. Use CSS classes like `.logo-isotype-white`, `.logo-wordmark-terracotta`, etc. so they can be reused throughout the page.

**Favicon:** Generate a favicon from the isotype. Create a `<link rel="icon">` using a base64-encoded small version of the isotype SVG (charcoal fill on transparent). Also add an SVG favicon: `<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,..."` with the isotype inline.

---

### CRITICAL REQUIREMENTS

1. **Inline ALL SVGs.** Read every `.svg` file in the project and embed the markup. No external `<img src="*.svg">` — the file must be 100% self-contained.

2. **Keep every existing feature from v1.3 intact:**
   - Loading screen animation (update to use the **isotype** instead of the combined logo — the flower animating in is more elegant)
   - Hero parallax effect
   - Sticky dot navigation with section indicators
   - Intersection Observer scroll-triggered animations
   - 4 flip cards in the Valores section
   - Click-to-copy HEX + CMYK in Paleta de Colores
   - Open Graph meta tags (keep og-image.png reference)
   - Mobile responsive + prefers-reduced-motion
   - Google Fonts: Playfair Display (400, 700) + Montserrat (300, 400, 500)

3. **Design system — use these CSS variables throughout:**
   ```css
   :root {
       --color-bone: #F2F0E9;
       --color-charcoal: #333333;
       --color-terracotta: #C78D76;
       --color-sage: #A4B0A0;
   }
   ```

4. **Aesthetic: European Bistro / Japandi / Silent Luxury.** Generous whitespace, refined typography, subtle animations. Nothing loud. No emoji in the UI (they appear only in tone-of-voice "don't" examples and roadmap status indicators). Consistent with v1.3's visual language.

---

### NEW & UPDATED SECTIONS (build in this order)

**Section 1 — Hero UPDATE:**
- Add a kicker line ABOVE the main title:
  - Text: `Bienvenida, Cristina. Esta es la visión de tu marca.`
  - Style: small uppercase Montserrat, wide letter-spacing (0.3em), fade-in animation with slight delay after the loading screen
- In the hero, use the **isotype** (flower) small and centered above the **wordmark** (`name_logo.svg` inline) — stacked vertically with elegant spacing. This replaces the combined logo for a more refined composition.

**Section 7 — "Normativa Técnica" (NEW — after Identidad Visual):**
- **Clear Space diagram:** Show the inline combined logo SVG with dashed border lines indicating minimum padding. Use the height of the letter "A" as the measurement unit. Label it "Área de Seguridad."
- **Minimum sizes table:** Digital: 40px height · Print: 1.5cm · Serigrafía: 2cm
- **Incorrect Uses — 2×2 grid:** Render the inline combined logo SVG 4 times with CSS transforms to show "don'ts":
  1. "No Distorsionar" → `transform: scaleX(1.5)`
  2. "No Rotar" → `transform: rotate(15deg)`
  3. "No Bajo Contraste" → `opacity: 0.2` on a light background
  4. "No Cambiar Colores" → apply a non-brand fill color (e.g., bright blue `#2196F3`)
- Each incorrect use gets a subtle red diagonal strike-through line (CSS pseudo-element) and a label below.

**Section 8 — "Versatilidad de Marca" (NEW — after Normativa Técnica):**
- 3-column responsive grid (stacks on mobile):
  1. Bone background `#F2F0E9` → dark charcoal **combined logo** → label: "Packaging / Papelería"
  2. Terracotta background `#C78D76` → white **combined logo** → label: "Stickers / Acentos"
  3. Sage background `#A4B0A0` → white **combined logo** → label: "Corporativo"
- Each card has rounded corners, subtle shadow, and the logo centered with generous padding.

**Section 9 — "Sistema Gráfico" (NEW — after Versatilidad):**

This section is now COMPLETE — no more placeholders. It showcases the full logo system:

- **9a. "Arquitectura de Marca" — Logo Components (3-column layout):**
  Show the 3 logo types side by side (stacks on mobile), each in a clean card:
  1. **Isotipo** — the flower (`isotype_logo.svg` inline, charcoal fill). Label: "Isotipo · Uso independiente en favicon, stickers, marcas de agua"
  2. **Logotipo** — the wordmark (`name_logo.svg` inline, charcoal fill). Label: "Logotipo · Uso en papelería formal, headers"
  3. **Logo Completo** — the combined logo (`logo-bakery.svg` inline, charcoal fill). Label: "Logo Completo · Uso principal en todas las aplicaciones"

- **9b. "Variantes de Color" — Color Variations Grid:**
  Show ALL logo variations in a responsive grid. For each of the 3 logo types, show the 5 color variants (original, white on dark card, charcoal, terracotta, sage). That's a 3×5 grid on desktop (or a tabbed/toggle interface — use buttons to switch between Isotipo / Logotipo / Logo Completo, showing the 5 color variants below). Include the HEX value and a short use-case label under each.

- **9c. Brand Pattern Strip:**
  Create a CSS-only repeating decorative band using brand colors (geometric: thin lines, dots, or minimal shapes in terracotta/sage on bone). Show it as a horizontal strip (~80px tall) that could be used on packaging edges. ALSO create a secondary pattern variant using the isotype at very low opacity (0.05-0.08) tiled as a watermark pattern — show both side by side.

**Section 13 — "Redes Sociales y Presencia Digital" (NEW — before Zona de Cliente):**
- **Instagram Phone Mockup:** CSS phone frame (rounded rect with notch) containing a 3×3 grid of Unsplash bakery images:
  - `https://images.unsplash.com/photo-1626265774643-f1943311a86b`
  - `https://images.unsplash.com/photo-1595928607828-4c3114ba5a22`
  - `https://images.unsplash.com/photo-1516919549054-e08258825f80`
  - Fill remaining 6 cells with brand-colored placeholders in alternating bone/sage/terracotta tones (some can have the isotype watermark centered at low opacity for realism)
- **Posting Strategy panel (beside the phone on desktop, below on mobile):**
  - Frecuencia: 3–4 posts/semana
  - Mejores horarios: 10 am · 2 pm · 7 pm
  - Hashtags: #AtelierMTY #ReposteríaDeDetalle #LujoSilencioso
  - Pilares de Contenido: 40% Producto · 25% Proceso · 20% Filosofía · 15% Comunidad (render as a small horizontal stacked bar chart in CSS using brand colors)
- **Caption Examples:**
  - ✅ "Tres días de preparación para un momento perfecto."
  - ❌ "¡¡PROMO 2X1 HOY!! 🔥🔥"
- **Download CTA:** Button "Descargar Estrategia Social Media (PDF)" → `href="#"` placeholder, styled as outline button in terracotta.

**Section 14 — "Zona de Cliente" (NEW — THIS IS THE MOST IMPORTANT NEW SECTION):**
- Professional dashboard-style download hub. Cristina needs to feel the project is organized and complete.
- 6 download cards in a responsive grid (3 cols desktop, 2 cols tablet, 1 col mobile):

  | Card Title | Format Label | Description | Status |
  |------------|-------------|-------------|--------|
  | Master Vectors | .AI / .EPS | Logos editables para imprenta | 🔒 Fase 2 |
  | Kit Digital | .PNG / .SVG | Logos para redes y presentaciones | ✅ Disponible |
  | Manual de Marca | .PDF | Manual de uso y estrategia | ✅ Disponible |
  | Pack Social Media | .PSD / Canva | Plantillas editables para posts | 🔒 Fase 2 |
  | Kit de Fotografía | .PDF | Guía de estilo fotográfico | 🔒 Fase 2 |
  | Papelería | .AI / .PDF | Tarjetas, membrete, facturas | 🔒 Fase 2 |

- "Disponible" cards: Active hover state, download icon, `href="#"` link, full-opacity styling.
- "Fase 2" cards: Lock icon, muted/desaturated styling, subtle "Próximamente" label, no hover effect.
- All links are `href="#"` placeholders for now.

**Section 15 — "Próximos Pasos" (NEW — after Zona de Cliente, before Footer):**
- Visual horizontal timeline/roadmap (vertical on mobile):
  - **Fase 1 ✅** Identidad Visual · Manual de Marca · Portal Web · Isotipo
  - **Fase 2 🔄** Papelería · Templates Social Media · Badge Logo
  - **Fase 3 📋** Packaging · Mockups · Material Impreso
- Use connecting lines or dots between phases. Fase 1 is highlighted/active (now includes Isotipo since it's done), Fase 2 and 3 are dimmed.

**Section 16 — Footer UPDATE:**
- Keep dark background.
- Use the **white isotype** (flower) as a subtle decorative element centered above the **white wordmark** — stacked vertically (mirroring the hero composition). This replaces the old combined logo.
- Add two CTA buttons side by side:
  1. "Descargar Kit de Marca (AI + PDF)" → outline style, `href="#"`
  2. "Aprobar esta dirección" → filled terracotta, `href="mailto:cristina@placeholder.com?subject=Aprobación%20ATELIER%20v2.0"`
- Version indicator: "Manual v2.0 — Febrero 2026"
- Footer text: "ATELIER. Est. 2026. Monterrey, MX."

---

### CURATED UNSPLASH IMAGES
Use these specific URLs where background/decorative images are needed:
- Hero texture: `https://images.unsplash.com/photo-1558961363-fa8fdf82db35?q=80&w=2065`
- Origin/hands: `https://images.unsplash.com/photo-1507048331197-7d4febed500e?q=80&w=1500`
- Product gallery (for IG mockup + photography section):
  - `https://images.unsplash.com/photo-1626265774643-f1943311a86b`
  - `https://images.unsplash.com/photo-1595928607828-4c3114ba5a22`
  - `https://images.unsplash.com/photo-1516919549054-e08258825f80`

---

### DOT NAVIGATION UPDATE
Update the sticky dot nav to include all 16 sections. Use abbreviated Spanish labels on hover.

### LOADING SCREEN UPDATE
Replace the combined logo in the loading screen with the **isotype** (flower). Animate it: fade in + subtle scale from 0.8 to 1.0, then after a beat, fade out and reveal the page. More elegant than the full combined logo.

---

### FINAL SECTION ORDER
```
1.  Hero ("Bienvenida, Cristina" + isotype + wordmark stacked)
2.  Esencia de Marca (Misión / Visión)
3.  Nuestros Valores (4 flip cards)
4.  Personalidad ("El Creador Intimista")
5.  Tono de Voz (Do's / Don'ts)
6.  Identidad Visual (Logo showcase)
7.  Normativa Técnica (Clear space, incorrect uses)         ← NEW
8.  Versatilidad de Marca (Logo on 3 backgrounds)           ← NEW
9.  Sistema Gráfico (Architecture, variants, patterns)      ← NEW (COMPLETE)
10. Paleta de Colores (Click-to-copy)
11. Tipografía (Font hierarchy)
12. Fotografía (Style guide)
13. Redes Sociales y Presencia Digital (IG mockup, strategy) ← NEW
14. Zona de Cliente (Download hub)                           ← NEW
15. Próximos Pasos (Roadmap timeline)                        ← NEW
16. Footer (CTAs, version, approval button)                  ← UPDATED
```

### OUTPUT
Save as `index-v2.0.html` in the project root. Single file only — all CSS in `<style>`, all JS in `<script>`, all SVGs inline. No external dependencies except Google Fonts CDN and Unsplash image URLs.

## PROMPT END — COPY TO HERE ↑
