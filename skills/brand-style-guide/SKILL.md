---
name: brand-style-guide
description: Creates or audits a simple visual identity, with colors, fonts, spacing, logo rules, and voice, and turns it into design tokens a website can use.
---

# Brand Style Guide

Use this when the user wants to define a look for their brand, check that a site matches its
brand, or turn brand choices into code.

## Steps

1. **Understand the brand.** Ask: who it's for, three words it should feel like, and two
   brands they admire (and why). Collect any existing logo, colors, or fonts.
2. **Define the identity:**
   - **Colors:** a primary, a neutral range (5–7 steps from background to text), one accent,
     and status colors (success, warning, error). Check text contrast (4.5:1).
   - **Type:** a heading font and a body font (free Google Fonts are fine), with a type
     scale (for example 14 / 16 / 20 / 28 / 40 / 56).
   - **Spacing and shape:** a spacing scale and one corner-radius style.
   - **Logo use:** minimum size, clear space, and which versions go on light and dark
     backgrounds.
   - **Imagery:** what photos or illustrations fit, and what to avoid.
   - **Voice:** three adjectives, plus one example sentence of how the brand sounds and one
     of how it never sounds.
3. **Turn it into tokens:** CSS variables (or a Tailwind theme) for colors, fonts, sizes,
   spacing, and radius, including a dark mode if wanted.
4. **For an audit:** compare the live site or files against the guide and list mismatches,
   most visible first.

## Output

A one-page guide (sections above), then the token code. Keep it short enough that someone
will actually use it.
