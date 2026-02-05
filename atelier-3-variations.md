# ATELIER — 3 Brand Variations for Client Review

**Purpose:** Create 3 different versions of the brand website so Cristina can choose her favorite direction.

**Output Files:**
- `index-v1-original.html` — Current version (Crema + Sage)
- `index-v2-warm.html` — Warm/Terracotta dominant
- `index-v3-cool.html` — Cool/Elegant Navy

**Base:** Use `index1.3.html` as the template for all versions.

---

## VERSION 1: ORIGINAL (Already Done)
**File:** `index-v1-original.html`
**Mood:** Japandi, Neutral, Earthy

Copy the current `index1.3.html` to `index-v1-original.html` — no changes needed.

### Color Palette V1
```css
--color-bone: #F2F0E9;        /* Background */
--color-charcoal: #333333;    /* Text */
--color-terracotta: #C78D76;  /* Accent */
--color-sage: #A4B0A0;        /* Secondary */
```

---

## VERSION 2: WARM TERRACOTTA
**File:** `index-v2-warm.html`
**Mood:** Warm, Inviting, Bakery-forward, Mediterranean

### Color Palette V2
```css
--color-bone: #FDF8F3;        /* Warmer cream, almost white */
--color-charcoal: #3D2C29;    /* Warm brown-black (chocolate) */
--color-terracotta: #C46E4E;  /* Richer terracotta (more rust) */
--color-sage: #D4A574;        /* Golden caramel (replaces sage) */
```

### Additional Changes for V2
1. **Hero section:** Use a warmer background tint
2. **Accent color usage:** Terracotta becomes more prominent (buttons, highlights)
3. **Footer background:** Use `#3D2C29` (warm chocolate) instead of charcoal
4. **Value cards hover:** Use golden caramel (`#D4A574`) as the flip background
5. **Section dividers:** Add subtle warm gradient transitions

### V2 Vibe Keywords
- Panadería artesanal
- Calidez de hogar
- Mediterráneo
- Dulce de leche
- Canela y vainilla

---

## VERSION 3: COOL ELEGANT
**File:** `index-v3-cool.html`
**Mood:** Sophisticated, French Patisserie, Luxury, Cool-toned

### Color Palette V3
```css
--color-bone: #F5F5F5;        /* Cool gray-white */
--color-charcoal: #1A1A2E;    /* Deep navy-black */
--color-terracotta: #8B7355;  /* Muted taupe/bronze (replaces terracotta) */
--color-sage: #6B7B8C;        /* Steel blue-gray (replaces sage) */
```

### Additional Changes for V3
1. **Hero section:** Cooler, more dramatic feel
2. **Typography:** Consider using slightly more letter-spacing for elegance
3. **Footer background:** Use deep navy `#1A1A2E`
4. **Value cards hover:** Use steel blue-gray (`#6B7B8C`) as flip background
5. **Accent usage:** Bronze/taupe for highlights instead of terracotta
6. **Overall feel:** More "French patisserie" than "cozy bakery"

### V3 Vibe Keywords
- Patisserie française
- Lujo silencioso
- Sofisticación urbana
- Elegancia fría
- Minimalismo europeo

---

## IMPLEMENTATION INSTRUCTIONS

### Step 1: Create Version 1 (Original)
```bash
cp index1.3.html index-v1-original.html
```

### Step 2: Create Version 2 (Warm)
1. Copy `index1.3.html` to `index-v2-warm.html`
2. Find the `:root` CSS section
3. Replace the color variables with V2 palette:
```css
:root {
    --color-bone: #FDF8F3;
    --color-charcoal: #3D2C29;
    --color-terracotta: #C4six6E4E;
    --color-sage: #D4A574;
}
```
4. Update the color palette section in the HTML content to show the new colors and their names:
   - "Crema Hueso" → "Crema Cálida" (#FDF8F3)
   - "Carbón Suave" → "Chocolate" (#3D2C29)
   - "Terracota" → "Terracota Intenso" (#C4six6E4E)
   - "Salvia" → "Caramelo Dorado" (#D4A574)

5. Update CMYK values in the color cards:
   - Crema Cálida: 0, 2, 4, 1
   - Chocolate: 0, 27, 32, 76
   - Terracota Intenso: 0, 44, 60, 23
   - Caramelo Dorado: 0, 23, 46, 17

### Step 3: Create Version 3 (Cool)
1. Copy `index1.3.html` to `index-v3-cool.html`
2. Find the `:root` CSS section
3. Replace the color variables with V3 palette:
```css
:root {
    --color-bone: #F5F5F5;
    --color-charcoal: #1A1A2E;
    --color-terracotta: #8B7355;
    --color-sage: #6B7B8C;
}
```
4. Update the color palette section in the HTML content:
   - "Crema Hueso" → "Gris Perla" (#F5F5F5)
   - "Carbón Suave" → "Azul Noche" (#1A1A2E)
   - "Terracota" → "Bronce Suave" (#8B7355)
   - "Salvia" → "Azul Acero" (#6B7B8C)

5. Update CMYK values in the color cards:
   - Gris Perla: 0, 0, 0, 4
   - Azul Noche: 42, 42, 0, 82
   - Bronce Suave: 0, 18, 39, 45
   - Azul Acero: 22, 10, 0, 45

6. Optional: Add `letter-spacing: 0.05em` to h1, h2 elements for extra elegance

---

## DEPLOYMENT

After creating all 3 versions, push to GitHub:

```bash
git add index-v1-original.html index-v2-warm.html index-v3-cool.html
git commit -m "Add 3 brand color variations for client review"
git push
```

### Shareable Links (after push)
- **V1 Original:** https://stevenoakstone-cio.github.io/atelier/index-v1-original.html
- **V2 Warm:** https://stevenoakstone-cio.github.io/atelier/index-v2-warm.html
- **V3 Cool:** https://stevenoakstone-cio.github.io/atelier/index-v3-cool.html

---

## COMPARISON SUMMARY

| Aspect | V1 Original | V2 Warm | V3 Cool |
|--------|-------------|---------|---------|
| **Background** | Crema Hueso #F2F0E9 | Crema Cálida #FDF8F3 | Gris Perla #F5F5F5 |
| **Text** | Carbón #333333 | Chocolate #3D2C29 | Azul Noche #1A1A2E |
| **Accent** | Terracota #C78D76 | Terracota Intenso #C4six6E4E | Bronce #8B7355 |
| **Secondary** | Salvia #A4B0A0 | Caramelo #D4A574 | Azul Acero #6B7B8C |
| **Mood** | Japandi neutral | Warm bakery | French luxury |
| **Feels like** | Zen tea house | Grandmother's kitchen | Parisian patisserie |

---

## MESSAGE FOR CRISTINA

Once ready, send her this message:

---

**Hola Cristina! 🎨**

Te preparé 3 opciones de paleta de colores para ATELIER. Cada una mantiene la esencia de "lujo silencioso" pero con diferentes vibras:

**Opción 1 - Original (Japandi):**
[Link V1]
→ Neutro, zen, equilibrado. Como un café de especialidad japonés.

**Opción 2 - Cálida (Mediterránea):**
[Link V2]
→ Más acogedora, tonos dorados y terracota. Como una panadería artesanal italiana.

**Opción 3 - Elegante (Francesa):**
[Link V3]
→ Sofisticada, tonos fríos y azulados. Como una patisserie parisina.

¿Cuál sientes que representa mejor a ATELIER? También podemos mezclar elementos de diferentes opciones.

---

## NOTES

- All versions use the same logo files (the gray logo works with all palettes)
- For V3 (Cool), you may want to create a navy-tinted logo version later if Cristina chooses it
- The white logo for footer works with all dark backgrounds
- Font choices remain the same across all versions (Playfair + Montserrat)
