---
name: Architectural Draft
colors:
  surface: '#f9f9f7'
  surface-dim: '#dadad8'
  surface-bright: '#f9f9f7'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f4f4f2'
  surface-container: '#eeeeec'
  surface-container-high: '#e8e8e6'
  surface-container-highest: '#e2e3e1'
  on-surface: '#1a1c1b'
  on-surface-variant: '#4c4546'
  inverse-surface: '#2f3130'
  inverse-on-surface: '#f1f1ef'
  outline: '#7e7576'
  outline-variant: '#cfc4c5'
  surface-tint: '#5e5e5e'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#1b1b1b'
  on-primary-container: '#848484'
  inverse-primary: '#c6c6c6'
  secondary: '#506600'
  on-secondary: '#ffffff'
  secondary-container: '#c1f100'
  on-secondary-container: '#546b00'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#002022'
  on-tertiary-container: '#00929b'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e2e2e2'
  primary-fixed-dim: '#c6c6c6'
  on-primary-fixed: '#1b1b1b'
  on-primary-fixed-variant: '#474747'
  secondary-fixed: '#c3f400'
  secondary-fixed-dim: '#abd600'
  on-secondary-fixed: '#161e00'
  on-secondary-fixed-variant: '#3c4d00'
  tertiary-fixed: '#7df4ff'
  tertiary-fixed-dim: '#00dbe9'
  on-tertiary-fixed: '#002022'
  on-tertiary-fixed-variant: '#004f54'
  background: '#f9f9f7'
  on-background: '#1a1c1b'
  surface-variant: '#e2e3e1'
typography:
  headline-xl:
    fontFamily: Bricolage Grotesque
    fontSize: 64px
    fontWeight: '800'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Bricolage Grotesque
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Bricolage Grotesque
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
  body-lg:
    fontFamily: Hanken Grotesk
    fontSize: 20px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Hanken Grotesk
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.0'
    letterSpacing: 0.1em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 8px
  gutter: 24px
  margin-mobile: 20px
  margin-desktop: 64px
  section-gap: 120px
---

## Brand & Style
This design system centers on a "Human-Made Minimalist" aesthetic, blending the precision of architectural drafting with the warmth of a hand-sketched notebook. It targets creative professionals, architects, and developers who value the process as much as the result.

The visual style is **Minimalist-Sketch**. It utilizes high-contrast monochrome layouts to evoke the feeling of ink on paper, punctuated by "highlighter" accents that guide the eye to critical actions. The atmosphere is intentional, raw, and intellectual, avoiding the sterile perfection of standard digital interfaces in favor of irregular, organic linework and generous whitespace.

## Colors
The palette is rooted in a "Paper and Ink" philosophy. 
- **Primary:** Pure black (#000000) for all linework, borders, and primary text, mimicking architectural ink pens.
- **Secondary (Highlighter Yellow):** Used for primary calls to action and "active" states, appearing as if a physical marker was dragged across the screen.
- **Tertiary (Blueprint Cyan):** Used for secondary highlights, links, or technical callouts.
- **Neutral (Paper):** A very slightly off-white (#F9F9F7) background with a subtle, non-repeating grain texture to simulate heavy cardstock.

## Typography
Typography creates a tension between the "Draft" and the "Final." 
- **Headlines:** Use **Bricolage Grotesque**. Its quirky, expressive terminals mimic the character of manual lettering while remaining legible.
- **Body:** Use **Hanken Grotesk**. This provides a clean, professional counterpoint to the more eccentric headlines, ensuring long-form content is easy to digest.
- **Technical Accents:** Use **JetBrains Mono** for labels, captions, and small metadata to reinforce the "technical drawing" or "wireframe" feel.

## Layout & Spacing
The layout follows a **Fixed Grid** model to simulate a drawing board. Elements are aligned to a strict 12-column grid, but their internal borders break that grid with "wavy" irregularities.

- **Desktop:** 12 columns with 64px outer margins.
- **Mobile:** 4 columns with 20px outer margins.
- **Rhythm:** Use a baseline of 8px. Spacing between major sections should be expansive (120px+) to allow the "sketch" elements room to breathe without looking cluttered.
- **Asymmetry:** Occasionally offset elements by 4-8px from the grid line to enhance the hand-drawn, imperfect feel.

## Elevation & Depth
This design system rejects shadows and blurs. Depth is achieved through **Stacking and Line Weight**:
- **Level 0 (Canvas):** The base paper texture.
- **Level 1 (Sections):** Defined by a 1px "wavy" black border.
- **Level 2 (Popovers/Modals):** Defined by a 2px solid black border with a "hard" 4px offset black block shadow (non-diffused) to simulate a paper cutout lifted off the page.
- **Highlighter Depth:** Use a semi-transparent "Secondary" color fill (multiply blend mode) behind text to simulate a highlighter pen being used on the paper.

## Shapes
While the system uses a `soft` base roundedness (0.25rem), the defining characteristic is the **Imperfect Path**. 
- All borders must be rendered with an SVG filter or custom path that introduces slight "wobble" and "overshoot" (where lines extend slightly past the corners, like a quick architectural sketch).
- Avoid perfect geometric circles; use slightly squashed "organic" ovals for radio buttons and icons.

## Components
- **Buttons:** Rectangular with a 2px "sketchy" border. On hover, the "Secondary" highlighter color fills the background with a slight bleed outside the border.
- **Input Fields:** A simple horizontal "ink" line that overshoots the container width. Labels sit above in `label-caps`.
- **Cards:** Use a 1px irregular border. Content inside uses generous padding (32px) to maintain the minimalist aesthetic.
- **Checkboxes:** Hand-drawn "X" marks rather than checkmarks.
- **Icons:** Custom-drawn with "open paths" (lines that don't quite touch) and variable stroke widths to mimic a felt-tip pen.
- **Progress Bars:** Represented as a series of hand-drawn hatch marks (/////) that fill in as the process completes.
