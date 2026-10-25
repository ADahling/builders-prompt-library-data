---
title: "Reverse-Engineering a Design System's Color Palette"
slug: reverse-engineering-a-design-system-s-color-palette
stage: Build
category: "Website Cloning"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/reverse-engineering-a-design-system-s-color-palette
---
# Reverse-Engineering a Design System's Color Palette

Extract and document the core color palette from a target design system to understand its visual hierarchy and implementation standards.

Variables: design_system_url

## Prompt

You are a UI/UX designer. Your task is to reverse-engineer the color palette from a well-known design system and document it.

Context:
- The design system to analyze is {{design_system_url}}.
- You need to identify the primary, secondary, accent, and neutral colors.
- Use a browser's developer tools to inspect the colors used in various components.

Provide:
1. A list of all the colors in the palette with their hex codes.
2. A brief description of how each color is used in the design system.

If you cannot open {{design_system_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

A practical exercise for designers to understand how color is used in a systematic way.
