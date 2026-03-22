# Design System Specification: Sophisticated Organic

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Atelier."** 

Moving away from the aggressive, high-contrast "luxury" tropes of black and gold, this system embraces a "Sophisticated Organic" aesthetic. It is designed to feel like a high-end physical space—think lime-washed walls, linen textures, and darkened oak. We achieve a premium feel not through decoration, but through **intentional restraint**. 

The design breaks the "template" look by utilizing wide margins, asymmetrical editorial layouts, and a "No-Line" philosophy. By prioritizing generous whitespace and tonal depth over structural borders, the UI feels breathable, bespoke, and elite.

---

## 2. Colors & Tonal Architecture
The 'Terra' palette is rooted in nature. We use deep forest greens for authority and warm stones/creams for an approachable, tactile foundation.

### Palette Highlights (Material Design 3 Logic)
*   **Primary (`#18281e`):** Our "Deep Forest." Used for high-emphasis actions and key branding.
*   **Surface (`#fcf9f4`):** Our "Soft Cream." The primary canvas that prevents the clinical feel of pure white.
*   **Secondary (`#695c4d`):** Our "Warm Stone." Used for specialized accents and secondary information.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections. 
Boundaries must be created through background color shifts. For instance, a booking module (`surface-container-low`) should sit directly on the `surface` background. The distinction is made by the subtle shift in value, not a stroke.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, fine papers. 
*   **Level 0 (Background):** `surface` (#fcf9f4)
*   **Level 1 (Sections):** `surface-container-low` (#f6f3ee)
*   **Level 2 (Cards/Modals):** `surface-container-highest` (#e5e2dd) or `surface-container-lowest` (#ffffff) for a "pop" of brightness.

### The "Glass & Gradient" Rule
To add "soul," use subtle linear gradients on primary CTAs—transitioning from `primary` (#18281e) to `primary_container` (#2d3e33). For floating navigation or over-image overlays, apply **Glassmorphism**: 
*   **Background:** `surface` at 70% opacity.
*   **Effect:** Backdrop-blur (12px to 20px).

---

## 3. Typography: Editorial Precision
The typography uses **Manrope** (or Hebrew equivalents like **Assistant/Heebo**) to convey a clean, architectural feel.

*   **Display & Headline:** Use `display-lg` (3.5rem) with a `letter-spacing` of `-0.02em` for a tight, high-fashion look.
*   **Titles:** Always use `title-lg` or `title-md` for service names. Apply a generous `letter-spacing` of `0.05em` to uppercase sub-headers to evoke a premium scent-brand feel.
*   **Hierarchy as Identity:** Use high contrast in scale. Pair a large `display-sm` headline with a very small, wide-spaced `label-md` "category" tag above it.

---

## 4. Elevation & Depth: Tonal Layering
We reject heavy, muddy shadows. Depth is achieved through "Atmospheric Perspective."

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-lowest` card on a `surface-container` background. The slight increase in brightness creates a natural "lift."
*   **Ambient Shadows:** If an element must float (e.g., a floating "Book Now" button), use an extra-diffused shadow:
    *   **Blur:** 32px to 48px.
    *   **Color:** `on-surface` (#1c1c19) at **4% opacity**. It should feel like a soft glow, not a dark drop.
*   **The "Ghost Border":** If a button requires definition over a complex image, use `outline-variant` (#c3c8c2) at **20% opacity**. Never use 100% opaque lines.

---

## 5. Components & Primitive Styling

### Buttons (The Interaction Pillars)
*   **Primary:** `primary` background, `on-primary` text. Shape: `full` (pill) or `xl` (3rem). No border.
*   **Secondary:** `surface-container-highest` background. No border.
*   **Tertiary:** Text-only with an underline that is `outline-variant` at 30% opacity, appearing only on hover.

### Cards & Service Lists
*   **Rule:** Forbid divider lines between list items.
*   **Implementation:** Use `spacing-8` (2.75rem) between items to let the eye define the grouping. For service menus, use a `surface-container-low` background that changes to `surface-container-high` on hover.

### Input Fields
*   **Style:** Minimalist. No "box" container. Use a bottom-only `outline-variant` (20% opacity). When focused, the line transitions to `primary` and the label (using `label-md`) shifts upward with increased letter spacing.

### Bespoke Component: "The Signature Gallery"
A horizontal scrolling area for professional photography. Use `round-lg` (2rem) for images. Ensure images are never full-bleed; they should always be "framed" by the `surface` background to maintain an editorial feel.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts (e.g., a large image on the left, with text offset to the bottom-right).
*   **Do** use "High-Low" typography (pairing a very large font with a very small font).
*   **Do** use professional photography featuring natural lighting and texture (hair, wood, fabric).
*   **Do** respect the `spacing-24` (8.5rem) for section margins to maintain "Elite" breathing room.

### Don't
*   **Don't** use 1px solid borders or `#000000` shadows.
*   **Don't** use generic "Barber" icons (clippers, scissors). If icons are needed, use ultra-thin (1pt) custom line art.
*   **Don't** fill the entire screen with content. If a section is empty, let it stay empty—whitespace is a luxury.
*   **Don't** use "AI-style" saturated colors. Keep the palette muted and organic.