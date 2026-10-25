---
title: "Extract Design Tokens from Any Website"
slug: extract-design-tokens-from-any-website
stage: Build
category: "Website Cloning"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/extract-design-tokens-from-any-website
---
# Extract Design Tokens from Any Website

Analyze a target URL to generate a comprehensive Tailwind CSS configuration and CSS custom properties for a complete design token system.

Variables: target_url

## Prompt

You are a design systems engineer. Extract a complete design token system from the following website that can be directly imported into a Tailwind CSS config.

Target URL: {{target_url}}

Extract and organize:

1. **Colors** — Map to CSS custom properties:
   - Primary palette (50-950 shades)
   - Secondary palette
   - Neutral/gray palette
   - Semantic colors (success, warning, error, info)
   - Background and surface colors
   - Text colors (primary, secondary, muted)

2. **Typography** — Map to Tailwind font config:
   - Font families with fallback stacks
   - Font size scale (xs through 6xl)
   - Font weight scale
   - Line height scale
   - Letter spacing scale

3. **Spacing** — Map to Tailwind spacing config:
   - Base unit and scale
   - Component-specific spacing patterns

4. **Borders & Shadows**:
   - Border radius scale
   - Border widths
   - Box shadow definitions (sm, md, lg, xl)

5. **Breakpoints**:
   - Responsive breakpoint values
   - Container max-widths per breakpoint

6. **Animation**:
   - Transition durations
   - Easing functions
   - Keyframe animations

Output as a complete `tailwind.config.ts` extension and a `globals.css` with CSS custom properties. Include both light and dark mode tokens.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Extracts the complete design system as production-ready Tailwind config. Essential for pixel-perfect clones.
