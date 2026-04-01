# Design System: The Bureaucratic Whimsy Framework

## 1. Overview & Creative North Star: "The Digital Cubicle"
This design system is a love letter to the organized chaos of office life. Our Creative North Star is **"The Digital Cubicle"**—an aesthetic that bridges the gap between soul-crushing corporate monotony and the vibrant, rebellious inner life of an office worker.

To move beyond the "standard indie game" look, we reject the rigid, centered grid. Instead, we embrace **Intentional Asymmetry**. Interfaces should feel like a desk at 3:00 PM: items are grouped logically but slightly overlapping, tilted, and layered. We use a "Pixel-Art Spirit" rather than strict low-res constraints, utilizing high-fidelity typography against "blocky" supply-inspired containers to create a premium, editorial feel.

---

## 2. Colors: The "Fluorescent Glow" Palette
We contrast "Boring Office" neutrals with high-energy "Task" accents. 

*   **The Foundation:** `surface` (#fff5e4) and its variants provide the manila-folder and beige-plastic warmth of 1990s hardware.
*   **Task Accents:** `primary` (Sticky-Note Yellow), `secondary` (Highlighter Green), and `tertiary` (File-Folder Blue) are used exclusively for interactive elements and critical gameplay feedback.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Traditional borders feel like a spreadsheet; we want a desk. Boundaries must be defined solely through background color shifts. Use `surface-container-low` for large content areas and `surface-container-highest` for nested interactive zones.

### Signature Textures & Gradients
To avoid a "flat" vector look, apply a subtle noise grain (simulating paper or carpet) over `surface` layers. For main CTAs, use a linear gradient transitioning from `primary` (#705900) to `primary_container` (#fdd34d) at a 45-degree angle to give buttons a "satin" finish.

---

## 3. Typography: Professional but "Off"
The typography pair reflects the duality of Vitya’s life: a rigid geometric structure for titles and a highly legible, slightly soft sans-serif for the "fine print."

*   **Display & Headlines (Space Grotesk):** This is our "pixel-adjacent" font. Its quirky terminals and technical construction feel like a modernized dot-matrix printer. Use `display-lg` for big humorous interjections.
*   **Body & Titles (Be Vietnam Pro):** This provides the professional balance. It ensures that even when the game is being absurd, the player can clearly read puzzle instructions.
*   **The "Bureaucratic" Hierarchy:** 
    *   **Display/Headline:** Use for loud, chaotic office "announcements."
    *   **Label-MD/SM:** Use for "Fine Print" or "Legal Disclaimers" at the bottom of the UI to lean into the office humor.

---

## 4. Elevation & Depth: Tonal Stacking
Forget traditional shadows; we use **Tonal Layering** to represent the physical stacking of paperwork.

*   **The Layering Principle:** 
    *   **Level 0 (Desk):** `surface_dim` (#ded3bc)
    *   **Level 1 (The Folder):** `surface_container` (#f1e7d3) 
    *   **Level 2 (The Sticky Note):** `primary_container` (#fdd34d)
*   **The "Ghost Border":** If a separation is strictly required for accessibility, use the `outline_variant` (#b4ac9c) at **15% opacity**. This creates a "crease" effect rather than a "box" effect.
*   **Glassmorphism:** For "floating" notifications (e.g., Vitya’s internal thoughts), use `surface_container_lowest` at 85% opacity with a `20px` backdrop blur. This mimics the look of frosted acrylic desk organizers.

---

## 5. Components: Refined Office Supplies

### Buttons (The "Sticky Note" & "Folder Tab")
*   **Primary:** High-saturation `primary_container`. Roundedness: `sm` (0.125rem) to maintain a blocky, paper-cut feel. Use `title-md` typography.
*   **Secondary:** `secondary_container` (Highlighter Green). Use these for "Success" or "Complete Task" actions.
*   **Tertiary:** No background; just `on_surface` text with a `surface_variant` hover state.

### Input Fields (The "Form Entry")
*   **Styling:** Instead of a box, use a `surface_container_highest` background with a `bottom-only` border using `outline` (#7d7668). 
*   **Focus State:** The background shifts to `tertiary_fixed` (light blue) to simulate a "selected" cell in a spreadsheet.

### Cards (The "Clipboard")
*   **Constraint:** Absolutely no divider lines. 
*   **Structure:** Use vertical white space (`spacing-8`) to separate header text from body. A card is a single sheet of `surface_container_low`. To group items within it, use a slightly darker `surface_container`.

### Additional Theme Components
*   **The Manila Tab:** A navigation component where the active tab has a top-left radius of `xl` and a top-right radius of `none`, mimicking a file folder tab.
*   **The "Paperclip" Progress Bar:** A `tertiary` colored bar that "clips" onto the side of a container to show level progress.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace the Tilt:** Rotate "Sticky Note" components by 1–2 degrees randomly via code to break the digital grid.
*   **Use High Contrast:** Ensure `on_primary_container` text is used over `primary_container` for maximum gameplay readability.
*   **Stack Surfaces:** Use the full range of `surface_container_lowest` to `highest` to create a "paper pile" look.

### Don’t:
*   **Don't use 1px solid black borders.** It breaks the "Indie/Charming" atmosphere and makes it look like a wireframe.
*   **Don't use pure grey.** Always use our tinted neutrals (`surface` variants) to maintain the "warm, dusty office" vibe.
*   **Don't center everything.** Lean into left-aligned "Top-Heavy" layouts, reminiscent of official forms and memos.