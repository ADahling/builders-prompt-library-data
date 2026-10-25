---
title: "Improve UI Accessibility through WCAG Color Contrast Compliance"
slug: improve-ui-accessibility-through-wcag-color-contrast-compliance
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/improve-ui-accessibility-through-wcag-color-contrast-compliance
---
# Improve UI Accessibility through WCAG Color Contrast Compliance

Audit UI contrast failures and get current and required ratios, brand-aware color adjustments, and contrast checker validation guidance.

Variables: ui_section_description, target_wcag_level, brand_guidelines_link, current_color_palette

## Prompt

The `{{ui_section_description}}` section of our application has been flagged for failing WCAG color contrast guidelines, specifically not meeting the `{{target_wcag_level}}` level. This significantly impacts users with visual impairments and overall readability. Your task is to identify all non-compliant text and interactive elements within this section, propose specific color adjustments that meet the accessibility requirements, and ensure these changes align with the existing `{{brand_guidelines_link}}` as much as possible. You should demonstrate the use of a color contrast checker tool to validate your proposed changes. The goal is to provide a comprehensive set of color palette adjustments that improve accessibility without drastically altering the brand's visual identity. Consider background colors, text colors, link colors, and button states.

**Current Color Palette (example values):**
```json
{{current_color_palette}}
```

**Output Format:**
1.  **Identification of Non-Compliant Elements:** List specific UI elements (e.g., 'Primary Button Text on Background', 'Link Text on Body Background') that fail contrast checks. 
2.  **WCAG Contrast Ratios:** For each non-compliant element, state the current contrast ratio and the required `{{target_wcag_level}}` ratio. 
3.  **Proposed Color Adjustments:** For each identified element, suggest new foreground and/or background color values (in hex or RGB) that meet the `{{target_wcag_level}}`. Provide the new contrast ratio for verification. 
4.  **Integration with Brand Guidelines:** Explain how these color adjustments balance accessibility with the existing brand guidelines. 
5.  **CSS Implementation Example:** Provide a snippet of CSS demonstrating how these new colors would be applied, preferably using CSS variables for maintainability.

## Tips

This prompt addresses a critical accessibility concern: color contrast. It guides the user through identifying issues, using tools, and proposing compliant color adjustments while considering brand guidelines.
