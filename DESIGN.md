# Design System Strategy: The Digital Manifesto

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"Architectural Activism."** 

Unlike traditional political websites that rely on cluttered grids and aggressive primary reds, this system adopts a high-end editorial approach. It treats information as a monumental structure—stable, authoritative, and immovable. By combining the raw energy of a modern manifesto with the sophisticated layout of a premium broadsheet, we move away from "template" design into a bespoke digital experience. 

We break the standard grid through **intentional asymmetry** and **high-contrast typography scales**. Headlines are treated as graphic elements, often overlapping surface containers or pushing the boundaries of the viewport, creating a sense of urgency that feels professional rather than panicked.

## 2. Colors
The palette is built on "Industrial Urgency"—a sophisticated mix of deep slates, grounded bronzes, and crisp, atmospheric surfaces.

*   **Primary (`#384346`) & Primary Container (`#4F5A5E`):** These represent the "Deep Slate" of the movement—authoritative, heavy, and serious.
*   **Secondary (`#6D5C3D`):** A metallic, grounded bronze used for call-to-actions that require a "human" yet "historic" weight.
*   **Surface Hierarchy & Nesting:** We define space through weight, not lines.
    *   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. To separate content, use background shifts. A section should transition from `surface` to `surface-container-low` to define a new context.
    *   **Surface Tiers:** Treat the UI as stacked sheets of fine paper. A `surface-container-lowest` card should sit atop a `surface-container-low` background to create a soft, natural lift.
*   **The "Glass & Gradient" Rule:** To avoid a flat, "out-of-the-box" look, floating navigation elements or overlays must utilize Glassmorphism. Use `surface` colors at 80% opacity with a `20px` backdrop-blur. 
*   **Signature Textures:** For hero backgrounds or primary CTAs, apply a subtle linear gradient transitioning from `primary` to `primary_container`. This adds a "soul" to the color that flat hex codes cannot achieve.

## 3. Typography
The typographic voice is the "Strong Independent." We utilize a triple-font strategy to create clear editorial lanes.

*   **Display & Headlines (Space Grotesk):** This is our "Activist" voice. It is technical, bold, and slightly provocative. `display-lg` (3.5rem) should be used for core messaging, often with tight letter-spacing (-2%) to create a "wall of text" effect.
*   **Body & Titles (Inter):** The "Rational Voice." Inter provides a neutral, highly legible contrast to the aggressive headlines. Use `body-lg` (1rem) for long-form reading to maintain a premium, accessible feel.
*   **Labels (Work Sans):** The "Utility Voice." These are used for navigation and metadata. At `label-sm` (0.6875rem), they provide a technical "Swiss" look to the interface.

## 4. Elevation & Depth
In this design system, depth is a result of **Tonal Layering**, not artificial lighting.

*   **The Layering Principle:** Hierarchy is achieved by "stacking" surface tiers. For example, placing a `surface-container-highest` element against a `surface-dim` background creates an immediate focal point without the need for a single shadow.
*   **Ambient Shadows:** If a floating element (like a modal) is required, use a "Tinted Ambient Shadow." The shadow should be `24px` to `48px` in blur, at 6% opacity, using the `on-surface` color. This mimics natural light rather than a digital drop-shadow.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use the `outline-variant` token at 15% opacity. This creates a "suggestion" of a boundary that doesn't break the editorial flow.
*   **Glassmorphism:** Use backdrop blurs on `surface-container` tiers to allow the vibrant primary colors to bleed through, making the layout feel integrated and modern.

## 5. Components
Each component must feel like a custom-designed piece of a larger machine.

*   **Buttons**: 
    *   **Primary**: Solid `primary` background with `on-primary` text. Use the `md` (0.375rem) roundedness. No borders.
    *   **Secondary**: Solid `secondary` (bronze) for the "Activist" call to action.
    *   **States**: On hover, shift the background to `primary_container`. Avoid "grow" effects; use subtle color transitions.
*   **Input Fields**: Forgo the "boxed" look. Use a `surface-container-high` background with a `2px` bottom-only stroke in `primary` when focused. This maintains the "editorial" aesthetic.
*   **Cards**: Forbid divider lines. Use vertical white space (from the `12` or `16` spacing scale) to separate the headline from the body. A card is simply a `surface-container-lowest` container on a `surface` background.
*   **Manifesto Chips**: Use `tertiary_container` for tags or categories. They should be rectangular with `sm` (0.125rem) rounding to look like stamped labels.
*   **Progress Indicators**: For movement goals or fundraising, use a "Thick Bar" style using `primary` for the track and `secondary` for the progress, avoiding thin, "app-like" bars.

## 6. Do's and Don'ts

### Do:
*   **Embrace Negative Space:** Use the `20` (5rem) and `24` (6rem) spacing tokens to let "High-Contrast" typography breathe.
*   **Asymmetric Alignment:** Align headlines to the left while keeping body text centered in a narrower column to create visual tension.
*   **Tonal Context:** Always check the contrast between `on-surface` and `surface-container-highest` for readability.

### Don'ts:
*   **Don't Use 1px Dividers:** Never use a line where a background color shift or white space could work. Lines "trap" the eye; color shifts "guide" it.
*   **Don't Use High-Opacity Shadows:** Avoid the "floating card" look of 2014. If it looks like it’s hovering more than 2mm off the screen, the shadow is too dark.
*   **Don't Mix Display Fonts:** Never use Inter for a Headline-LG or Space Grotesk for Body-MD. The separation of "Voice" is sacred.
*   **No "App" Roundedness:** Avoid `full` (pill) shapes for anything other than specific action chips. High-end editorial design favors the stability of the `md` and `none` scales.