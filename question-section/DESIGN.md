# Design System Specification: The Cartographic Canvas

## 1. Overview & Creative North Star
The vision for this design system is **"The Cartographic Canvas."** In the context of "TopoTrainer.nl," we are moving beyond a standard educational tool to create a high-end, editorial experience that mirrors the precision and depth of modern cartography. 

Rather than a "template" of boxes, we treat the UI as a series of intentional, layered planes. We break the rigid SaaS grid through **intentional asymmetry**: utilizing wide margins, offset headers, and overlapping elements to create a sense of discovery. This system prioritizes breathing room and tonal depth, ensuring that the student feels focused, not overwhelmed.

---

## 2. Colors
Our palette is rooted in the "Deep Navy" of authority and the "Action Blue" of progress. We utilize a sophisticated Material-based tonal range to create a UI that feels alive and tactile.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders for sectioning or containment. Boundaries must be defined solely through background color shifts. For example, a `surface-container-low` sidebar sitting against a `surface` background. The eye should perceive structure through value changes, not "boxes."

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine paper or frosted glass. Use the following hierarchy to define importance:
*   **Base Layer:** `surface` (#f7f9ff)
*   **Structural Sections:** `surface-container-low` (#edf4ff)
*   **Interactive Cards:** `surface-container-lowest` (#ffffff)
*   **High-Priority Overlays:** `surface-container-highest` (#d1e4fb)

### The "Glass & Gradient" Rule
To escape the "standard SaaS" look, use **Glassmorphism** for floating elements (like navigation bars or hovering tooltips). Apply a semi-transparent `surface-variant` with a `backdrop-blur(12px)`. 

For Primary CTAs and Hero sections, use a **Signature Gradient** transitioning from `primary` (#006397) to `primary_container` (#3498db) at a 135-degree angle. This adds "visual soul" and a premium finish that flat colors cannot achieve.

---

## 3. Typography
We use **Inter** as our typographic anchor. It provides the mathematical precision required for an EdTech platform while maintaining an editorial elegance.

*   **Display (lg/md/sm):** Used for "Big Moments"—landing page headers or module titles. These should be set with tight letter-spacing (-0.02em) to feel authoritative.
*   **Headline & Title:** Used for lesson headers. Use `headline-lg` (2rem) for page titles, often offset with an asymmetric left margin to break the grid.
*   **Body (lg/md/sm):** Our primary information carrier. `body-lg` (1rem) is the standard for lesson content to ensure maximum readability for students.
*   **Labels (md/sm):** High-contrast, all-caps labels using `label-md` (0.75rem) with increased letter-spacing (0.05em) should be used for metadata like "MODULE 01" or "LEVEL: EXPERT."

---

## 4. Elevation & Depth
Depth in this system is achieved through **Tonal Layering** and light physics, not structural lines.

*   **The Layering Principle:** Stack `surface-container` tiers to create lift. A card (`surface-container-lowest`) placed on a section (`surface-container-low`) creates a soft, natural lift without the need for a shadow.
*   **Ambient Shadows:** When a "floating" effect is required (e.g., a modal or a primary action card), use an extra-diffused shadow. 
    *   *Formula:* `0px 20px 40px rgba(9, 29, 46, 0.06)` (using a 6% opacity of the `on-surface` color). This mimics natural ambient light rather than a synthetic grey drop shadow.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, it must be a **Ghost Border**. Use the `outline-variant` token at 15% opacity. Never use 100% opaque borders.
*   **Glassmorphism Depth:** For top-level navigation, use `surface_container_lowest` at 80% opacity with a `backdrop-blur-md` to allow the map or content colors to bleed through subtly.

---

## 5. Components

### Buttons
*   **Primary:** A gradient from `primary` to `primary_container`. No border. Roundedness: `md` (0.75rem). Height: 48px minimum.
*   **Secondary:** `surface_container_highest` background with `on_primary_container` text.
*   **Tertiary:** Ghost style. No background, `primary` text. Use for less critical actions.

### Cards & Lists
*   **Cards:** Use `surface_container_lowest`. **Strictly no dividers.** Use 2rem (`spacing.8`) of vertical white space to separate list items within a card.
*   **Selection Chips:** Use `secondary_container` for unselected and a vibrant `primary` with `on_primary` text for selected states.

### Input Fields
*   **Style:** Do not use outlined boxes. Use `surface_container_high` as a solid background fill. 
*   **States:** On focus, transition the background to `surface_container_lowest` and apply a 2px "Ghost Border" of `primary`.
*   **Touch Targets:** All inputs and interactive labels must maintain a minimum height of 48px to support touch-based learning.

### Specialized EdTech Components
*   **The Progress Track:** A custom horizontal element using `tertiary_fixed` (#7efba4) for completed stages and a subtle `surface_variant` for upcoming stages.
*   **The Map Insight Card:** A Glassmorphic card that overlays map sections, using a heavy `backdrop-blur` to maintain legibility over complex geographical textures.

---

## 6. Do's and Don'ts

### Do
*   **Do** use the Spacing Scale (specifically `spacing.6` and `spacing.8`) to create "content islands" instead of using divider lines.
*   **Do** use `on_surface_variant` for secondary text to maintain a sophisticated hierarchy.
*   **Do** align text-heavy content to a narrow, readable column (max 650px) while allowing cards and maps to bleed wider.

### Don't
*   **Don't** use pure black (#000000) for shadows or text. Always use the `on_surface` (#091d2e) or a tinted variant.
*   **Don't** use 1px borders to separate navigation from the body. Use a background color shift or a subtle ambient shadow.
*   **Don't** crowd the screen. If a student is learning, the UI should recede, leaving only the "Cartographic Canvas" and the primary action.