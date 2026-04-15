# Design System Specification: Lifestyle x Industrial Precision

## 1. Overview & Creative North Star
**Creative North Star: The Calibrated Sanctuary**
This design system rejects the "industrial-cold" aesthetic of traditional manufacturing in favor of a "lifestyle-warm" precision. It is built on the Japanese concept of *Ma* (negative space)—treating the void not as empty space, but as a structural element that provides breathing room for high-end technology. 

By merging the organic softness of a lifestyle brand with the rigorous accuracy of PET bottling engineering, we create a "Digital Curator" experience. We break the standard rigid grid through intentional asymmetry, where large-scale editorial typography overlaps airy, bright imagery, and components feel as though they are floating on a calm surface of water.

## 2. Colors & Tonal Architecture
The palette is a sophisticated blend of natural indigo and muted sage, anchored by a spectrum of "living whites."

### The "No-Line" Rule
To maintain a premium, seamless feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined solely through background color shifts or tonal transitions. For instance, a section utilizing `surface-container-low` (#f3f4f5) should sit directly against a `surface` (#f8f9fa) background. This creates a soft, architectural division rather than a hard, mechanical one.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine Washi paper.
- **Base Layer:** `surface` (#f8f9fa)
- **Content Cards:** `surface-container-lowest` (#ffffff) to provide a crisp, clean lift.
- **Secondary Interaction Areas:** `surface-container` (#edeeef) or `surface-container-high` (#e7e8e9).

### The "Glass & Gradient" Rule
To elevate the "Industrial Precision" aspect, use Glassmorphism for floating navigation or overlays. Apply a `surface` color at 70% opacity with a `24px` backdrop blur. 
**Signature Texture:** For primary CTAs or hero backgrounds, utilize a subtle linear gradient transitioning from `primary` (#143363) to `primary-container` (#2e4a7b) at a 135-degree angle. This adds "visual soul" and depth that flat color cannot replicate.

## 3. Typography & The Editorial Rhythm
The typography system uses a dual-font approach to balance human-centric lifestyle with technical authority.

*   **Display & Headlines (Plus Jakarta Sans):** These are the "Precision" elements. Large, bold, and airy. Use `display-lg` (3.5rem) for hero statements with a `-0.02em` letter spacing to feel tight and engineered.
*   **Body & Labels (Manrope):** These are the "Lifestyle" elements. Manrope offers a geometric yet friendly tone.
*   **The Editorial Edge:** Use `label-md` (#44474f) with a generous `0.1em` letter spacing for sub-headers or category tags to create a high-end magazine feel.

## 4. Elevation & Depth
Depth is achieved through **Tonal Layering** rather than traditional structural shadows.

### The Layering Principle
Place a `surface-container-lowest` (#ffffff) element on top of a `surface-container-low` (#f3f4f5) background. The 1% shift in brightness provides a soft, natural lift that mimics natural light hitting a physical object.

### Ambient Shadows
When a floating effect is required (e.g., for a high-priority Modal), use "Ambient Shadows":
- **Blur:** 32px to 64px
- **Opacity:** 4% - 8%
- **Color:** Use a tinted version of `on-surface` (#191c1d) rather than pure black to ensure the shadow feels like a part of the environment.

### The "Ghost Border" Fallback
If a border is required for accessibility in complex data views, use the **Ghost Border**: `outline-variant` (#c4c6d0) at **15% opacity**. Never use 100% opaque borders.

## 5. Components

### Buttons (The Precision Tactile)
- **Primary:** Background: `primary` (#143363) gradient; Text: `on-primary` (#ffffff); Corners: `DEFAULT` (0.5rem).
- **Secondary:** Background: `secondary-container` (#d0e4da); Text: `on-secondary-container` (#54675e).
- **Tertiary (Ghost):** No background; Text: `primary` (#143363); subtle `0.05em` letter spacing.

### Cards & Lists (The Flow)
- **Rule:** **Strictly no divider lines.** Use vertical white space (32px or 48px) to separate list items.
- **Card Styling:** Use `surface-container-lowest` with a `lg` (1rem) corner radius. On hover, transition the background to `surface-bright` and apply an Ambient Shadow.

### Input Fields
- **Background:** `surface-container-low` (#f3f4f5).
- **Indicator:** Instead of a full box border, use a 2px bottom-only stroke in `primary` (#143363) when focused to mimic a technical drawing.
- **Labels:** Always use `label-md` sitting 8px above the input.

### Glass Navigation
For top-level navigation, use a `surface` tint with `blur(20px)`. This allows the vibrant "Lifestyle" imagery (water, tea) to bleed through the UI, softening the industrial edges.

## 6. Do’s and Don’ts

### Do:
- **Asymmetric Balance:** Place a large `display-md` headline on the left and a small, high-quality image of water droplets on the right, leaving 40% of the screen as white space.
- **Tinted Neutrals:** Use `surface-variant` for backgrounds to keep the design from feeling "stark-white" or "hospital-clean."
- **High-Quality Imagery:** Use photography with high key lighting (bright and airy). Precision machinery should be shot with a shallow depth of field to make it feel approachable.

### Don’t:
- **No Heavy Outlines:** Do not wrap components in high-contrast boxes.
- **No Pure Grays:** Avoid #000000 or #808080. Use the `indigo` and `sage` tinted neutrals provided in the palette.
- **No Cramming:** If a section feels full, increase the padding by 1.5x. In this system, space is a luxury.
- **No Standard Shadows:** Never use the default "Drop Shadow" presets in design tools. Always manually craft the Ambient Shadow with low opacity and high blur.