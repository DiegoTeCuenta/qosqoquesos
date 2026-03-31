# Design System: Editorial Artisan

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Modern Alchemist."** It is a visual philosophy that bridges the raw, earthy heritage of the Peruvian Andes with a sophisticated, high-end editorial digital experience. 

Traditional templates rely on rigid grids and heavy borders; this system breaks that mold through **intentional asymmetry and tonal depth**. We treat the screen not as a flat surface, but as a series of curated layers. By using parallax effects and overlapping elements (e.g., product photography breaking out of its container), we evoke the rugged, multi-layered terrain of the Qosqo region. The goal is to make the user feel they are browsing a premium physical lookbook rather than a standard e-commerce catalog.

## 2. Colors
Our palette is rooted in the high-contrast natural world of Peru—deep forest shadows, brilliant sun-drenched grain, and soft mountain mists.

*   **Primary (#173809 & #2D4F1E):** Represents the fertile earth and forest. Used for deep-toned sections and primary actions.
*   **Secondary (#7B5800 & #FEBB10):** The golden glow of artisan products and Andean sun. Used for highlights, active states, and high-visibility CTAs.
*   **Surface & Neutrals (#FDF9F0 to #E6E2D9):** A range of creams and off-whites that mimic fine parchment or stone, providing a breathable, premium backdrop.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders are strictly prohibited for sectioning. Definition between content areas must be achieved solely through shifts in background tokens (e.g., a `surface-container-low` card placed atop a `surface` background). If you feel the need for a line, use whitespace (`spacing-8`) instead.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the `surface-container` tiers to define depth:
*   **Base:** `surface` (#fdf9f0)
*   **Secondary Section:** `surface-container-low` (#f7f3ea)
*   **Feature Card:** `surface-container-highest` (#e6e2d9)
Nesting these creates a natural, soft shadow-less hierarchy.

### The "Glass & Gradient" Rule
To add "soul," use subtle gradients for large hero areas, transitioning from `primary` (#173809) to `primary_container` (#2D4F1E). For floating navigation or product overlays, apply **Glassmorphism**: use `surface` at 70% opacity with a `20px` backdrop-blur to allow Andean landscape textures to bleed through.

## 3. Typography
The type system creates a dialogue between the "Traditional" (Serif) and the "Modern" (Sans-Serif).

*   **Display & Headlines (Newsreader):** A characterful, bold serif. Use this for product names and editorial storytelling. The slight irregularities in the serif forms evoke hand-crafted quality.
*   **Titles & Body (Manrope):** A clean, high-legibility sans-serif. Manrope’s modern geometry balances the serif's weight, ensuring that even dense nutritional information feels airy and approachable.
*   **Labeling:** All labels should use `label-md` (Manrope) with a slight tracking increase (+0.05rem) to maintain an upscale, catalog feel.

## 4. Elevation & Depth
We eschew traditional drop shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-high` section. This creates a "soft lift" that feels architectural rather than digital.
*   **Ambient Shadows:** If a floating effect is required (e.g., for the WhatsApp CTA), use a shadow with a 32px blur at 6% opacity, tinted with the `primary` color (#173809) rather than black.
*   **The "Ghost Border" Fallback:** For accessibility in form fields, use the `outline_variant` token at **15% opacity**. Never use a 100% opaque border.

## 5. Components

### WhatsApp CTA (Signature Component)
The most prominent action. 
*   **Background:** `secondary` (#7B5800) or a glassmorphic primary green.
*   **Style:** Floating Action Button (FAB) style with an `xl` (0.75rem) corner radius.
*   **Shadow:** Large ambient shadow to ensure it sits above the parallax background.

### Product Cards
*   **Background:** `surface-container-lowest` (#ffffff).
*   **Border:** None.
*   **Padding:** `spacing-5` (1.7rem) to provide an editorial "breath."
*   **Interaction:** On hover, a subtle shift to `surface-container-low` and a `2px` upward translation.

### Buttons
*   **Primary:** `primary` background with `on_primary` text. `md` roundedness.
*   **Secondary:** `secondary_container` background. Use for "Add to Inquiry."
*   **Tertiary:** Ghost style using `primary` text with no background.

### Lists & Price Menus
*   **Rule:** Forbid divider lines.
*   **Layout:** Use `spacing-4` between items. Align prices to the far right using `title-md` (Manrope) to create a clear vertical scan line without the need for visual "crutches" like dots or lines.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts where product photography overlaps text containers.
*   **Do** apply `parallax` effects to Andean landscape backgrounds to create a sense of vast space.
*   **Do** use "white space" as a functional element to group related artisan food items.
*   **Do** use `Newsreader` for large-scale pricing (S/.) to make the cost feel like a curated value.

### Don't:
*   **Don't** use 1px solid black or grey borders. They break the organic feel of the artisan brand.
*   **Don't** use "pure black" (#000000) for text. Always use `on_surface` (#1C1C17) for a softer, more premium look.
*   **Don't** overcrowd the cards. If a product description is long, use a "Read More" trigger rather than shrinking the typography.
*   **Don't** use standard Material ripples. Use soft opacity fades for touch states to maintain the sophisticated tone.