# Design System Document: Editorial Cyber-Gold

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Kinetic Archive."** 

Moving away from the static, traditional layout of the provided CV, this system translates professional experience into a high-octane, editorial digital experience. It rejects the "template" look by utilizing intentional asymmetry, oversized typography, and a "Black Hole" depth model—where the pure `#000000` background acts as an infinite void for high-contrast, gold-leafed technical details to float within. This is not a resume; it is a high-tech manifesto of a web developer's capabilities.

## 2. Colors
The palette is built on extreme contrast to ensure the developer's work feels premium and definitive.

*   **Primary Hierarchy:** Use `primary` (#ffe792) for high-impact accents and `primary_container` (#ffd709) for core branding elements. This mimics the "Gold" requirement but adds tonal depth.
*   **The "No-Line" Rule:** Designers are strictly prohibited from using 1px solid borders to separate sections. We define space through "Tonal Shifts." For example, a project gallery section should transition from `background` (#0e0e0e) to `surface_container_low` (#131313) to create a boundary-less transition.
*   **Surface Hierarchy & Nesting:** Treat the interface as physical layers. 
    *   *Base:* `surface_dim` (#0e0e0e)
    *   *Nested Content:* Place `surface_container_high` (#1f1f1f) cards inside a `surface_container_low` section to create natural, soft lift.
*   **The "Glass & Gradient" Rule:** Use Glassmorphism for floating navigation bars or tech-stack chips. Combine `surface_variant` (#262626) at 60% opacity with a `backdrop-blur` of 20px. 
*   **Signature Textures:** Apply a subtle linear gradient from `primary_dim` (#efc900) to `primary` (#ffe792) on large "Call to Action" buttons to give them a metallic, forged appearance rather than a flat digital fill.

## 3. Typography
The system uses a pairing of **Space Grotesk** (Display/Headlines) and **Manrope** (Body).

*   **Display & Headline (Space Grotesk):** This typeface provides the "high-tech" professional edge. Use `display-lg` (3.5rem) for the developer's name and `headline-lg` (2rem) for major CV sections like "EXPERIENCE." Tighten letter-spacing (tracking) by -2% for headlines to achieve an editorial feel.
*   **Body & Title (Manrope):** Chosen for its clean, geometric legibility. `body-lg` (1rem) should be used for project descriptions. 
*   **Labeling (Space Grotesk):** Use `label-md` (0.75rem) in all-caps with 10% tracking for metadata (e.g., "DATES," "TECHNOLOGIES," "LOCATION"). This creates a "technical blueprint" aesthetic.

## 4. Elevation & Depth
In this design system, depth is a result of light behavior, not structural boxes.

*   **The Layering Principle:** Avoid shadows on standard cards. Instead, use the `surface-container` tiers. A card using `surface_container_highest` (#262626) placed on `surface` (#0e0e0e) provides all the visual separation needed.
*   **Ambient Shadows:** For floating elements like Modals or Hero Photos, use a shadow with a 40px blur, 0px offset, and 8% opacity using the `primary` color. This creates a "Gold Glow" rather than a dark shadow.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline_variant` (#484848) at **15% opacity**. It should be barely perceptible—felt rather than seen.
*   **Glassmorphism:** Use semi-transparent `surface_bright` (#2c2c2c) for overlaying elements (like a sticky header) to allow the "Gold" highlights of the content below to bleed through softly as the user scrolls.

## 5. Components

### Buttons
*   **Primary:** Background: Gradient `primary_dim` to `primary`. Text: `on_primary_fixed` (#453900). Radius: `sm` (0.125rem) for a sharp, aggressive tech look.
*   **Secondary:** Background: `none`. Border: Ghost Border (outline-variant @ 20%). Text: `primary`.

### Chips (Tech Stack)
*   **Style:** Use `surface_container_highest` background with `label-sm` typography. 
*   **Asymmetry:** Use a `full` roundedness on the left side but a `sm` (0.125rem) radius on the right side to break the standard pill-shape convention.

### Experience Timeline
*   **Forbid Dividers:** Do not use lines to separate "Iris Digital" from "FPT Polytechnic." Instead, use `surface_container_low` for the background of even-numbered entries and `background` for odd-numbered entries.

### Input Fields
*   **State:** Background should be `surface_container_lowest` (#000000). On focus, the bottom edge should glow with a 2px `primary` line—no other borders.

### Cards (Project Showcase)
*   **Structure:** No borders. Use the photo of the developer or project screenshot as a full-bleed background with a `surface_dim` gradient overlay at the bottom to house the text.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical margins. For example, align headline text to the far left (10% margin) but body text to a central column (25% margin).
*   **Do** use `primary` color (#ffe792) sparingly. It should feel like a "laser" in the dark, highlighting only the most critical information (e.g., job titles or CTA buttons).
*   **Do** utilize the `xl` (0.75rem) roundedness only for large containers, keeping smaller elements at `sm` (0.125rem) for a precision-engineered feel.

### Don't:
*   **Don't** use pure white (#ffffff) for long-form body text. Use `on_surface_variant` (#ababab) to reduce eye strain against the black background.
*   **Don't** use standard 12-column grids. Experiment with 5 or 7 column offsets to create a "custom-coded" look that reflects the developer's skill.
*   **Don't** use traditional "Drop Shadows" (Black/Grey). If an element needs to pop, use a gold-tinted ambient glow or a tonal background shift.