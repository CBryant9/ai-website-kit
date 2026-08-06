# DESIGN.md — Website Design System

Fill this in before asking Claude to build any UI. Every field matters.
If you are not sure what to put, pick a brand from github.com/VoltAgent/awesome-design-md and copy their DESIGN.md instead of filling this in from scratch.

---

## Visual Direction

Write 2-3 sentences describing the overall feel. Example: "Minimal, editorial, high contrast. Lots of white space. Feels expensive and calm — professional without being corporate. No startup clichés."

YOUR DIRECTION:
[fill in]

---

## Colors

Primary background: #[hex] — [what it's used for, e.g., "main page background"]
Secondary background: #[hex] — [e.g., "card surfaces, section alternates"]
Primary text: #[hex] — [e.g., "all body copy"]
Secondary text: #[hex] — [e.g., "captions, metadata, muted labels"]
Accent / CTA: #[hex] — [e.g., "buttons, links, highlights — use sparingly"]
Error / warning: #[hex]
Success: #[hex]

---

## Typography

Heading font: [font name] [weight] — [where to find it, e.g., "Google Fonts"]
Body font: [font name] [weight]
Mono font (if used): [font name]

Type scale:
- h1: [size]px / [weight]
- h2: [size]px / [weight]
- h3: [size]px / [weight]
- Body: [size]px / [weight] / [line-height]
- Small / label: [size]px / [weight]

---

## Spacing

Base unit: [e.g., 8]px
Scale: [e.g., 8 / 16 / 24 / 32 / 48 / 64 / 96 / 128]px
Section padding (desktop): [e.g., 80]px top/bottom
Section padding (mobile): [e.g., 48]px top/bottom
Max content width: [e.g., 1200]px

---

## Borders and Radius

Default border color: #[hex]
Border style: [e.g., 1px solid]
Radius scale:
- None: 0px
- Small (inputs, tags): [e.g., 4]px
- Default (buttons, cards): [e.g., 8]px
- Large (modals, feature blocks): [e.g., 16]px
- Pill: 999px

---

## Shadows

None: none
Subtle: [e.g., 0 1px 3px rgba(0,0,0,0.08)]
Default: [e.g., 0 4px 12px rgba(0,0,0,0.10)]
Strong: [e.g., 0 8px 32px rgba(0,0,0,0.16)]

---

## Rules — Do Not Break These

List the things Claude must never do visually:
- [e.g., No gradient buttons]
- [e.g., No hero images with text overlaid directly on the photo]
- [e.g., No purple — it reads as generic AI aesthetic]
- [e.g., No Inter font — pick something with personality]
- [e.g., No nested card-inside-card-inside-card layouts]
- [add your own]

---

## Component Notes

Buttons: [describe the style — e.g., "solid fill in accent color, no icon unless essential, hover darkens 10%"]
Nav: [e.g., "clean horizontal, no dropdown menus, sticky on scroll"]
Cards: [e.g., "light border, subtle shadow on hover, no gradient fills"]
Forms: [e.g., "1px border, rounded 6px, focus ring in accent color"]
