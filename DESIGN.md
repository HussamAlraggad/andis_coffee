---
name: Andis Coffee
description: QR table menu and brand surfaces for Andis Coffee in Jubeiha, Amman
colors:
  primary: "#4C5A3E"
  primary-deep: "#3A4730"
  bg-cream: "#faf8f5"
  bg-category: "#f4f1ec"
  ink: "#1a1a1a"
  ink-muted: "#666666"
  ink-dim: "#888888"
  border-light: "#d9d2c9"
  border-card: "#e8e2da"
  card-bg: "#ffffff"
  white: "#ffffff"
  bg-dark: "#1a1a1a"
  text-dark: "#e8e2da"
  surface-dark: "#222222"
  border-dark: "#333333"
  accent-dark: "#8a9a7a"
typography:
  display:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontWeight: 600
    fontSize: "clamp(1.75rem, 5vw, 2.5rem)"
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Alexandria, system-ui, -apple-system, sans-serif"
    fontWeight: 400
    fontSize: "0.9rem"
    lineHeight: 1.6
  label:
    fontFamily: "Alexandria, system-ui, -apple-system, sans-serif"
    fontWeight: 600
    fontSize: "0.65rem"
    textTransform: "uppercase"
    letterSpacing: "0.1em"
rounded:
  sm: "4px"
  md: "6px"
  lg: "8px"
spacing:
  xs: "0.375rem"
  sm: "0.5rem"
  md: "0.75rem"
  lg: "1rem"
  xl: "2rem"
components:
  category-button:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: "0.5rem 0.875rem"
    fontWeight: 600
    fontSize: "0.75rem"
  category-button-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    rounded: "{rounded.md}"
  menu-item:
    borderBottom: "1px dashed {colors.border-light}"
    padding: "0.55rem 0"
  highlight-card:
    backgroundColor: "{colors.card-bg}"
    border: "1px solid {colors.border-card}"
    rounded: "{rounded.lg}"
    padding: "0.75rem"
  footer-link:
    backgroundColor: "transparent"
    textColor: "{colors.white}"
    border: "1px solid #ffffff40"
    rounded: "{rounded.md}"
    padding: "0.4rem 0.9rem"
---

# Design System: The Green Lounge

## 1. Overview

**Creative North Star: "The Green Lounge"**

A warm, earthy refuge. The design system for Andi's Coffee is a calm, confident visual identity built around a deliberate green (#4C5A3E) — the colour of a well-kept cafe, not a corporate brand. It feels like walking into a space where craft matters: the wood is oiled, the coffee is measured, and every surface has a place.

The system is warm and earthy but never rustic. Clean and calm but never cold. Bold in its green commitment but cozy in its texture. It carries the tactile confidence of a printed cafe menu — no glassmorphism, no gradient text, no AI-generated beige-on-beige templates.

**Key Characteristics:**
- Committed green palette that carries 30-60% of the surface
- Serif display + warm sans body pairing
- Flat surfaces with tonal layering, no shadows
- Bilingual by default (Arabic RTL + English LTR)
- Mobile-first, instantly loading, zero dependency

## 2. Colors

A committed palette anchored by a deliberate olive-green. The green is not an accent — it's the surface. Warmth comes from the green body, not from a tinted beige background.

### Primary
- **Olive Grove** (#4C5A3E): The brand green. Used for the header, active category buttons, footer, and price labels. Carries 30-40% of surface area.
- **Olive Deep** (#3A4730): A darker variant for dark mode header and footer, maintaining contrast without shifting hue.

### Neutral
- **Cream Paper** (#faf8f5): The body background. Barely tinted toward the green hue (chroma < 0.02), warm without being beige-by-default.
- **Warm Stone** (#f4f1ec): Category navigation background, one step darker than Cream Paper. Used for the sticky scroll bar.
- **Ink Black** (#1a1a1a): Body text. Full contrast against all light backgrounds.
- **Warm Mid** (#666666): Secondary text for item descriptions and metadata.
- **Warm Dim** (#888888): Lowest-priority text (highlight descriptions, credits).

### Border & Surface
- **Linen** (#d9d2c9): Dashed borders between menu items. Soft enough to not compete.
- **Sand** (#e8e2da): Card borders in highlights section.
- **Snow** (#ffffff): Card backgrounds and text on green backgrounds.

### Dark Mode
- **Night Sky** (#1a1a1a): Page background in dark mode.
- **Warm Ash** (#e8e2da): Body text in dark mode.
- **Deep Surface** (#222222): Card and surface backgrounds in dark mode.
- **Slate** (#333333): Borders in dark mode.
- **Muted Sage** (#8a9a7a): Price and accent text in dark mode.

### Named Rules
**The Green Commitment Rule.** The primary green is not an accent — it IS the brand. It occupies the header, the active state, the footer, and price labels. Its prevalence is deliberate, not decorative.

**The No-Beige Rule.** The background is Cream Paper tinted toward green, not generic beige. If the background looks like every other cafe site, it's wrong.

## 3. Typography

**Display Font:** Cormorant Garamond (Georgia, serif)
**Body Font:** Alexandria (system-ui, -apple-system, sans-serif)

**Character:** The pairing is deliberate contrast — a refined serif for headings that feels like a cafe chalkboard, paired with a warm, Arabic-friendly geometric sans for body text. Both families support Arabic natively, making the bilingual experience seamless.

### Hierarchy
- **Display** (600, clamp(1.75rem, 5vw, 2.5rem), 1.2, -0.02em): Page title in the header. `text-wrap: balance` to avoid orphans.
- **Headline** (600, 1.35rem, 1.3, -0.01em): Section headings (menu category titles). Uses Cormorant Garamond.
- **Title** (600, 1.25rem, 1.3): Footer heading and secondary titles.
- **Body** (400, 0.9rem, 1.6): Menu item names and body copy. Max line length 65-75ch.
- **Body Small** (400, 0.8rem, 1.5): Footer text, secondary descriptions.
- **Label** (600, 0.65rem, uppercase, 0.1em): Section numbers and category labels. Tiny but deliberate.
- **Item** (500, 0.9rem): Menu item name. bolder than body to stand out.
- **Price** (600, 0.9rem): Price text. Same size as item name but bolder, green.

## 4. Elevation

The system is flat by default. Depth is conveyed through tonal layering (light backgrounds against the cream body, tinted category nav, card borders) rather than shadows. This keeps the interface feeling physical and printed — like a well-designed paper menu, not a digital dashboard.

Dark mode uses the same flat approach: surfaces are distinguished by lightness steps, not by shadow depth.

## 5. Components

### Category Buttons
- **Shape:** Gently rounded (6px radius).
- **Default:** Transparent background, green text.
- **Active:** Green background (Olive Grove #4C5A3E), white text.
- **States:** Hover adds a 15% green tint (`#4C5A3E15`). No shadow, no outline.
- **Layout:** Horizontal scroll with hidden scrollbar, flex-shrink-0 to prevent wrapping.

### Menu Items
- **Style:** Flex row with item name left, price right. Dashed bottom border (Linen #d9d2c9) between items, no border on the last item.
- **Typography:** Item name in body weight 500, price in bold 600 green.
- **Width:** Max 640px container centered on the page for comfortable reading.

### Highlight Cards
- **Shape:** Rounded corners (8px radius), white background, 1px Sand (#e8e2da) border.
- **Layout:** 2-column grid with 0.5rem gap on mobile, full width on larger screens.
- **States:** Static only — no hover interaction needed for informational cards.
- **Internal padding:** 0.75rem.

### Language Toggle
- **Style:** Inline button in the header, small (0.75rem), transparent with a subtle white border (40% opacity).
- **Hover:** 15% white overlay.
- **Behaviour:** Instant client-side toggle with no page reload. Updates `lang`, `dir`, and all content via the same data store.

### Footer Links
- **Style:** Inline buttons on green background, small (0.8rem), transparent with 40% opacity white border, 6px radius.
- **Hover:** 15% white overlay.
- **Spacing:** Centered flexbox row with 1rem gap, wraps on mobile.

## 6. Do's and Don'ts

### Do:
- **Do** use the green (#4C5A3E) as the dominant brand colour across header, footer, and active states.
- **Do** show every menu price immediately — no taps, no reveals, no interaction required.
- **Do** support English and Arabic as equals with instant toggle and no reload.
- **Do** load the menu in under 2 seconds on Jordanian 3G/4G — no JS frameworks, no external dependencies beyond web fonts.
- **Do** use flat surfaces with tonal layering instead of shadows.
- **Do** keep the background tinted toward the green hue, not generic beige.

### Don't:
- **Don't** hide prices behind taps or interaction.
- **Don't** use heavy React SPAs that blank out on slow networks.
- **Don't** use PDF menus requiring pinch-zoom on mobile.
- **Don't** use beige-on-beige AI-generated cafe palettes, Fraunces fonts, or glassmorphism.
- **Don't** use gradient text, side-stripe borders, or numbered section markers as decoration.
- **Don't** add decorative elements that don't serve the menu — no emoji, no animations that delay content visibility, no cards nested inside cards.
- **Don't** require JavaScript to render core content — the noscript fallback must show the menu.
