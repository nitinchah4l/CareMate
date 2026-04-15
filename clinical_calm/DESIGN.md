# Design System Documentation: The Clinical Sanctuary

## 1. Overview & Creative North Star
This design system is built upon the North Star of **"The Clinical Sanctuary."** In an industry often defined by clinical coldness or cluttered complexity, this system moves in the opposite direction. It prioritizes visual silence, authoritative editorial layouts, and a sense of "breathable" trust.

We avoid the "generic app" look by rejecting traditional rigid grids in favor of intentional asymmetry and varying tonal depths. The goal is to make the user feel like they are stepping into a high-end, private healthcare suite—where every piece of information is curated, and the interface recedes to let the data (and the person) breathe.

---

## 2. Colors & Tonal Architecture
The palette is rooted in a professional medical blue, but it is executed through a sophisticated hierarchy of "Surfaces" rather than lines.

### The Palette
- **Primary Canvas:** `primary` (#004ac6) for high-impact brand moments; `primary_container` (#2563eb) for interactive primary elements.
- **Tonal Neutrals:** Use `surface` (#f7f9fb) as the foundational background. Secondary information should sit on `surface_container_low` (#f2f4f6).
- **Accent & Emotion:** `tertiary` (#943700) is reserved for "Human Moments"—wellness tips, community insights, or personalized coaching—to provide warmth against the professional blue.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section off content. 
Boundaries must be defined through:
1. **Background Color Shifts:** A `surface_container_lowest` (#ffffff) card sitting on a `surface` (#f7f9fb) background creates an organic boundary.
2. **Negative Space:** Use the spacing scale to create "rivers" of white space that naturally guide the eye.

### The "Glass & Gradient" Rule
To elevate the experience from "standard" to "premium":
- **CTAs:** Use subtle linear gradients transitioning from `primary` to `primary_container` to give buttons a "tactile soul."
- **Floating Elements:** Use Glassmorphism for overlays or navigation bars. Apply a semi-transparent `surface_container_lowest` with a `backdrop-blur` of 12px–20px to allow the medical blue to bleed through softly.

---

## 3. Typography: Editorial Authority
We use **Inter** not as a standard UI font, but as an editorial tool. The hierarchy is designed to convey immediate clarity and calm authority.

- **Display Scales (`display-lg` to `display-sm`):** Reserved for data-heavy "Hero" moments, such as a heart rate number or a wellness score. These should feel monumental.
- **Headline & Title:** Use `headline-md` for page titles to establish a strong "top-down" hierarchy. Ensure generous line-height to maintain the "Sanctuary" feel.
- **Body & Label:** Use `body-lg` for all instructional text. Labels (`label-md`) should be used sparingly for metadata, always in `on_surface_variant` (#434655) to reduce visual noise.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are often a crutch for poor layout. In this design system, we achieve depth through **Tonal Layering**.

### The Layering Principle
Think of the UI as stacked sheets of fine paper. 
- **Base:** `surface` (#f7f9fb)
- **Sectioning:** `surface_container_low` (#f2f4f6)
- **Interactive Card:** `surface_container_lowest` (#ffffff)

### Ambient Shadows
When a "floating" effect is required (e.g., a critical Action Button), shadows must be:
- **Extra-Diffused:** Blur values should be 24px or higher.
- **Low-Opacity:** 4% to 8% opacity.
- **Tinted:** Instead of pure black, the shadow color should be a deep version of the `primary` color or `on_surface` to mimic natural light in a clean environment.

### The "Ghost Border" Fallback
If a boundary is required for accessibility (e.g., in high-contrast modes), use a **Ghost Border**: the `outline_variant` token at 15% opacity. Never use 100% opaque borders.

---

## 5. Components

### Cards & Containers
Cards are the heart of the "HealthMate" experience.
- **Corner Radius:** Use `xl` (1.5rem/24px) for primary container cards to feel soft and approachable. Use `lg` (1rem/16px) for nested elements within those cards.
- **Constraint:** No divider lines. Use `surface_container_high` for a subtle background shift if you must separate content within a card.

### Buttons
- **Primary:** Gradient from `primary` to `primary_container`. 16px (`lg`) rounded corners.
- **Secondary:** `surface_container_highest` background with `on_surface` text. No border.
- **Tertiary:** Text-only with `primary` color, used for low-emphasis actions like "View Details."

### Input Fields
- **Style:** Use a "Floating Label" approach. The field background should be `surface_container_low`. 
- **States:** On focus, the background shifts to `surface_container_lowest` (white) with a "Ghost Border" of `primary` at 40% opacity.

### Navigation & Progress (The "Health Curve")
- For medical progress (e.g., treatment cycles), avoid jagged lines. Use smooth, organic Bezier curves in `primary` to visualize health data, reinforcing the "calm" brand pillar.

---

## 6. Do’s and Don’ts

### Do:
- **Do** embrace asymmetry. A large headline on the left with a floating card offset to the right creates a premium, editorial feel.
- **Do** use `surface_tint` for subtle highlights on active navigation items.
- **Do** prioritize "Visual Breathing Room." If you think there is enough padding, add 8px more.

### Don’t:
- **Don’t** use pure black (#000000) for text. Always use `on_surface` (#191c1e) to maintain a soft, accessible contrast.
- **Don’t** use 1px dividers to separate list items. Use a 12px vertical gap or a subtle tonal shift.
- **Don’t** use standard "Error Red" for everything negative. Use `error_container` with `on_error_container` text to keep the UI from feeling "alarming"—we are a sanctuary, not an emergency room.

---
*Note to Junior Designers: This design system is about the "space between" elements as much as the elements themselves. Trust the tonal shifts and the typography to do the heavy lifting.*