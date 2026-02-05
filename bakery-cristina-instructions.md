# ATELIER — The Full Brand Experience
## Claude Code Prompt

Create a single-page interactive "Brand Pitch" website for ATELIER (a European Bistro / Japandi / Silent Luxury pastry brand). This site presents the full branding strategy to the client, Cristina.

OUTPUT: One file called `index.html` containing all HTML, CSS, and JavaScript.

---

## LOGO FILE

- File: `logo-bakery.svg` (already exists in project folder)
- **IMPORTANT:** The SVG contains BOTH a flower/symbol on top AND the text "ATELIER" below. Display the COMPLETE SVG (flower + text together) in the sticky nav (~50px height) and in Section 5 Visual Identity showcase.
- Do NOT extract just the text — use the full logo as-is.

---

## DESIGN SYSTEM (CSS Variables)

```css
:root {
  --color-bone: #F2F0E9;
  --color-charcoal: #333333;
  --color-terracotta: #C78D76;
  --color-sage: #A4B0A0;
  --font-heading: 'Playfair Display', serif;
  --font-body: 'Montserrat', sans-serif;
}
```

- Load fonts from Google Fonts with `font-display: swap`
- Japandi aesthetic: generous whitespace (padding), elegant typography, muted colors
- Alternating section backgrounds for rhythm: Bone → Sage → Bone → Sage → Bone

---

## SECTIONS (7 Total)

### SECTION 1: THE HOOK (Hero)
- Full-screen cinematic background image (Unsplash: macro meringue texture, beige pastry aesthetic)
- JS-driven parallax effect on background (with mobile fallback to static)
- Content (centered, fades in slowly):
  - Big Title (H1): "ATELIER."
  - Subtitle: "Repostería de Detalle."
  - Micro-copy: "Est. 2026 • Monterrey."
- Background: Use a desaturated/warm-toned bakery image

### SECTION 2: THE ORIGIN (Split Screen)
- Layout: **Left image (40-50%) / Right text (50-60%)**
- Image: Black & white or desaturated photo of hands working with dough (Unsplash)
- Apply a subtle grayscale or sepia CSS filter to the image
- Text content:
  - Headline (H2): "Todo empieza con una receta."
  - Body: "Lo que nació observando a mi madre hacer su mostachón, se convirtió en mi refugio. Encontré en la repostería la paz que da la precisión. No es solo cocinar; es un momento de conexión. Hoy, ATELIER es la evolución de esa herencia: perfeccionismo técnico con alma artesanal."
- Background: var(--color-bone)
- Text fades up on scroll

### SECTION 3: THE STRATEGY (Values Cards)
- Background: var(--color-sage)
- Headline (H2, centered): "Nuestros No Negociables."
- Layout: Grid of 4 cards (2x2 on desktop, 1 column on mobile)
- **Card Interaction:** Subtle fade/slide reveal on hover (NOT 3D flip) — content shifts or fades to show the back text. Keep it elegant.
- Card Content:
  1. Front: "Calidad Radical." → Back: "Si no es perfecto, no sale del taller. Preferimos no vender a vender algo a medias."
  2. Front: "Estética Silenciosa." → Back: "El amor entra por los ojos. El montaje es nuestra firma de autor."
  3. Front: "Honestidad." → Back: "Prometemos solo lo que podemos cumplir. Transparencia absoluta en ingredientes y procesos."
  4. Front: "El Proceso es Sagrado." → Back: "La limpieza y el orden no se negocian. La repostería es disciplina y respeto."
- Cards animate in staggered on scroll

### SECTION 4: THE PERSONALITY (Archetype)
- Background: var(--color-bone) with subtle paper texture (use CSS noise or subtle pattern)
- Headline (H2, centered): "El Creador Intimista."
- Body text (centered, max-width for readability): "Somos como esa anfitriona impecable que habla en voz baja, pero todos callan para escucharla. No gritamos para vender. Somos elegantes, sofisticados, pero con un guiño de calidez humana."
- **Quote Block** (styled blockquote with oversized quotation marks in terracotta):
  - "Dicen que la perfección no existe, pero tal vez no han probado nuestro equilibrio de texturas. Un pequeño capricho para su martes. (O miércoles, nadie lleva la cuenta)."
- Elements fade up on scroll

### SECTION 5: VISUAL IDENTITY (Design System Showcase)
- Background: var(--color-sage)
- Headline (H2): "Identidad Visual."

**Subsection A — Logo:**
- Display `logo-bakery.svg` prominently (the complete SVG with flower + text)
- Show it at a larger size (~150-200px height) as the "Main Logo"
- Add label: "Logotipo Principal"
- Note: If a secondary isotype is needed later, add a placeholder box labeled "Isotipo (próximamente)"

**Subsection B — Typography:**
- Show sample text in both fonts side by side:
  - Playfair Display: "La perfección está en los detalles" (labeled as "Títulos")
  - Montserrat: "La perfección está en los detalles" (labeled as "Cuerpo de texto")
- Show the pairing visually, not just "Aa"

**Subsection C — Color Palette:**
- 4 interactive circles in a row
- Each circle shows the color with its name below:
  - Crema Hueso (#F2F0E9)
  - Carbón Suave (#333333)
  - Terracota (#C78D76)
  - Salvia (#A4B0A0)
- Click to copy hex code with visual feedback (circle pulses + "¡Copiado!" tooltip appears briefly)

### SECTION 6: THE PRODUCT UNIVERSE (Masonry Gallery)
- Background: var(--color-bone)
- Headline (H2, centered): "El Universo Atelier."
- Layout: CSS Grid masonry-style (no JS library), Pinterest-inspired but cleaner
- 5 images with captions (use curated Unsplash photos — gourmet bakery, desserts, packaging aesthetic):
  1. Caption: "El Protagonista. Equilibrio dulce y ácido." (mostachón/tart style)
  2. Caption: "Unboxing: Un regalo para uno mismo." (packaging/box)
  3. Caption: "Indulgencia Moderna." (chunky cookies)
  4. Caption: "Sofisticación Rústica." (rustic tart/pay)
  5. Caption: "Para quien busca belleza, no solo azúcar." (lifestyle/aesthetic shot)
- **Lightbox:** Clicking any image opens a custom vanilla JS modal to view full size
- Images animate in staggered on scroll

### SECTION 7: FOOTER
- Background: var(--color-charcoal)
- Text color: var(--color-bone)
- Content (centered):
  - Tagline: "Listo para hornear ideas."
  - Credit: "Proyecto de Branding 2026"
- **Scroll to Top button:** Subtle arrow or "↑" that smoothly scrolls to hero when clicked

---

## INTERACTIONS & TECHNICAL REQUIREMENTS

### Animations (Intersection Observer)
- All text/cards/images start hidden (opacity: 0, translateY: 30px)
- On scroll into view: animate to opacity: 1, translateY: 0
- Use staggered delays for groups (cards, gallery items)
- Transition duration: 0.6s - 0.8s ease-out

### Navigation
- Sticky nav appears after scrolling past hero
- Left side: `logo-bakery.svg` (complete logo, ~40-50px height)
- Right side: Dot indicators (7 dots for 7 sections)
- Dots show current section (filled/highlighted)
- **Dots are clickable** — smooth scroll to that section
- **Hover tooltips** on dots showing section names: "Inicio", "Origen", "Estrategia", "Personalidad", "Identidad", "Productos", "Contacto"

### Page Load
- Optional: Brief fade-in on initial page load (0.5s) for cinematic feel
- Logo in nav can animate in after hero loads

### Accessibility
- `prefers-reduced-motion` media query to disable animations
- Proper heading hierarchy (h1 → h2 → h3)
- Alt text on all images
- Focus states for interactive elements

### Responsive
- Mobile-first approach
- Split screen (Section 2) stacks vertically on mobile
- Cards grid becomes single column on mobile
- Nav dots may hide or become a minimal indicator on very small screens
- Gallery adapts to single/double column on mobile

### General
- Semantic HTML5
- Modern CSS (Grid, Flexbox, custom properties)
- Vanilla JavaScript only (no frameworks)
- Smooth scroll behavior: `scroll-behavior: smooth`
- Use specific curated Unsplash photo URLs (not random) for consistent aesthetic

---

## CURATED IMAGE SUGGESTIONS

Use these Unsplash search terms for consistent aesthetic:
- Hero: "meringue macro", "beige pastry texture"
- Origin: "hands dough baking", "artisan baker hands" (apply grayscale filter)
- Gallery: "gourmet tart", "bakery packaging minimal", "chocolate chunk cookies", "rustic pie", "cafe aesthetic beige"

---

## SUMMARY CHECKLIST

- [ ] 7 sections with smooth scroll transitions
- [ ] Alternating background colors (Bone/Sage rhythm)
- [ ] Complete `logo-bakery.svg` (flower + text) in nav and Section 5
- [ ] Split screen layout for Origin story
- [ ] 4 hover-reveal value cards (subtle, not 3D flip)
- [ ] Elegant blockquote with terracotta quotation marks
- [ ] Typography showcase with sample sentences
- [ ] Interactive color palette (click to copy)
- [ ] Masonry gallery with lightbox
- [ ] Sticky nav with clickable dots + hover tooltips
- [ ] Scroll to top button in footer
- [ ] Reduced motion support
- [ ] Mobile responsive
