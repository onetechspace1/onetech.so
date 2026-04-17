# Design System Document: One Tech 'Coming Soon' Experience

## 1. Overview & Creative North Star
**Creative North Star: "The Visionary Pulse"**

To represent "One Vision. Smart Technology," this design system moves away from static, rigid grids and toward a "Visionary Pulse" aesthetic. This approach treats the digital interface as a living, breathing entity. We avoid the "template" look by utilizing high-contrast typography scales, intentional asymmetry, and deep, layered immersion. The goal is to make the user feel they are looking into a high-tech viewport rather than a flat website. 

The system leverages the tension between the deep navy (`surface`) and the vibrant magenta (`primary_container`), using the light pink (`primary`) as a sophisticated highlight that adds "glow" and "air" to the interface.

---

## 2. Colors & Surface Architecture

### The "No-Line" Rule
To maintain a premium, editorial feel, **1px solid borders are strictly prohibited** for sectioning or containment. Boundaries must be defined through:
- **Tonal Shifts:** Placing a `surface_container_low` card against a `surface` background.
- **Negative Space:** Using generous padding to allow content to "float" within its own gravitational field.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the surface-container tiers to create depth:
1.  **Base Layer:** `surface` (#0b1229) – The infinite dark canvas.
2.  **Structural Sections:** `surface_container_low` (#141a32) – For large content blocks.
3.  **Interactive Elements:** `surface_container_high` (#222941) – For cards and input containers.

### The "Glass & Gradient" Rule
For "Coming Soon" hero elements, use **Glassmorphism**. Apply `surface_variant` with a 40-60% opacity and a `backdrop-filter: blur(20px)`. 
**Signature Texture:** Main CTAs and the Hero graphic should utilize a linear gradient transitioning from `primary_container` (#D81E5B) to `secondary` (#F4B6C5) at a 135-degree angle to create a sense of forward-moving energy.

---

## 3. Typography: The Editorial Voice

We use a dual-font approach to balance "High-Tech" with "Trustworthy."

*   **Display & Headlines (Space Grotesk):** This sans-serif has a technical, geometric personality. Use `display-lg` for the "One Vision" statement to command authority. The wide apertures feel innovative and "open."
*   **Body & Titles (Manrope):** A modern, highly legible sans-serif. It provides the "Trustworthy" anchor. Use `body-lg` for the "Smart Technology" descriptions to ensure clarity.

**Hierarchy Strategy:** 
- Use **extreme scale**. A `display-lg` headline should sit in stark contrast to `body-md` supporting text to create a high-end, editorial cadence.
- Use `label-md` in all-caps with 0.1em letter-spacing for metadata or small "Coming Soon" tags.

---

## 4. Elevation & Depth: Tonal Layering

Traditional drop shadows are too "standard." This system uses **Ambient Light Physics**:

*   **Layering Principle:** Instead of shadows, stack `surface_container_lowest` (#060d24) cards inside `surface_container_high` (#222941) sections to create a "recessed" or "carved" look.
*   **Ambient Shadows:** If a floating element (like a modal or floating CTA) requires a shadow, it must use the `on_surface` color at 5% opacity with a `64px` blur. This creates an ethereal glow rather than a muddy shadow.
*   **The Ghost Border Fallback:** For buttons or inputs on dark backgrounds, use `outline_variant` at 15% opacity. This "Ghost Border" provides just enough definition for accessibility without breaking the fluid aesthetic.

---

## 5. Components

### Buttons
*   **Primary:** A vibrant `primary_container` (#D81E5B) background with `on_primary_container` text. Use `full` roundedness for a modern, sleek feel.
*   **Secondary (Glass):** `surface_variant` with 20% opacity and a `backdrop-filter: blur(10px)`. No border.
*   **Tertiary:** Text-only in `primary` (#FFB2BD) with an understated hover state using `surface_bright`.

### Input Fields (Subscription/Waitlist)
*   **Container:** Use `surface_container_highest`. 
*   **States:** On focus, the `outline` should glow with `primary` at 30% opacity. 
*   **No Dividers:** Label and input should be separated by vertical space, never a line.

### Cards & Lists
*   **Forbid Dividers:** Use `surface_container_low` vs `surface_container_high` to distinguish between list items.
*   **Interaction:** On hover, a card should shift from `surface_container_low` to `surface_container_bright` to signify life.

### Countdown/Progress Timer
*   A custom component for "Coming Soon." Use `display-md` for numbers and `label-sm` for units. Numbers should be in `primary_fixed`, creating a "lit from within" effect against the navy background.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts (e.g., text aligned left, hero element offset to the right) to feel custom and high-end.
*   **Do** use the `primary` (#FBBCCB) color for tiny accents—bullets, small icons, or a single word in a headline—to act as a visual "spark."
*   **Do** ensure a minimum 4.5:1 contrast ratio between `on_surface` text and the `surface` background.

### Don't:
*   **Don't** use 1px solid white or grey borders. They cheapen the "High-Tech" feel.
*   **Don't** use pure black (#000000). Always use the deep navy `surface` (#0B1229) to maintain tonal depth.
*   **Don't** clutter the screen. If an element doesn't serve the "One Vision," remove it. Premium design is about what you leave out.
*   **Don't** use standard "drop shadow" presets. If it looks like a default plugin, it’s wrong. Stick to tonal shifts.