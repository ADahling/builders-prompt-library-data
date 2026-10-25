---
title: "Ensure WCAG AA/AAA Color Contrast Compliance"
slug: ensure-wcag-aa-aaa-color-contrast-compliance
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ensure-wcag-aa-aaa-color-contrast-compliance
---
# Ensure WCAG AA/AAA Color Contrast Compliance

Audit UI color palettes for WCAG AA/AAA compliance and generate accessible hex code alternatives that maintain brand integrity.

Variables: wcag_level, ui_section_name, current_color_palette

## Prompt

You are tasked with auditing a specific section of a web application to ensure its color combinations meet WCAG (Web Content Accessibility Guidelines) AA or AAA contrast requirements. Analyze the provided color palette for background and foreground elements (text, icons, interactive components). Identify any instances where the contrast ratio falls below the required threshold for normal text (4.5:1 for AA, 7:1 for AAA) or large text (3:1 for AA, 4.5:1 for AAA). For each failing combination, propose specific alternative color values (hex codes) that achieve the desired contrast ratio while maintaining the application's brand identity as much as possible. Explain the original contrast issue and justify your new color suggestions with their calculated contrast ratios.

**Target WCAG Level:** {{wcag_level}} (e.g., 'AA', 'AAA')
**UI Section to Audit:** {{ui_section_name}} (e.g., 'header navigation', 'form error messages', 'data table')
**Current Color Palette (Background/Foreground Pairs):**
```json
{{current_color_palette}}
```

**Output Format:** For each problematic color pair, list the 'Original Colors', 'Original Contrast Ratio', 'WCAG Failure Reason', 'Proposed New Colors', 'New Contrast Ratio', and 'Justification'. Ensure all proposed colors are provided as hex codes.

## Tips

An intermediate prompt designed to help developers fix accessibility issues related to color contrast, crucial for inclusive design.
