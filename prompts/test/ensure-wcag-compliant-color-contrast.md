---
title: "Ensure WCAG Compliant Color Contrast"
slug: ensure-wcag-compliant-color-contrast
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 98
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/ensure-wcag-compliant-color-contrast
---
# Ensure WCAG Compliant Color Contrast

Analyze color pairs to verify WCAG 2.1 contrast compliance and generate accessible HEX/RGB alternatives that preserve brand aesthetics.

Variables: current_foreground_color, current_background_color, target_wcag_level, element_type

## Prompt

You are an accessibility consultant. Your task is to analyze the provided foreground and background color combination and determine if it meets the specified Web Content Accessibility Guidelines (WCAG) 2.1 contrast ratio requirements. If the current combination fails to meet the standard, suggest alternative color values for either the foreground or background (or both) that achieve compliance while attempting to maintain the original aesthetic intent as closely as possible. Provide the contrast ratio for the original and proposed colors, and explicitly state whether the proposed solution meets the target WCAG level.

**Current Foreground Color (HEX or RGB):** `{{current_foreground_color}}` (e.g., '#FF0000', 'rgb(255, 0, 0)')
**Current Background Color (HEX or RGB):** `{{current_background_color}}` (e.g., '#FFFFFF', 'rgb(255, 255, 255)')
**Target WCAG Level:** `{{target_wcag_level}}` (e.g., 'AA Large Text', 'AA Normal Text', 'AAA Normal Text')
**Type of Element:** `{{element_type}}` (e.g., 'Button text', 'Body paragraph', 'Heading')

**Output Format:** Provide a structured response with the following sections:
1.  **Current Contrast Analysis:**
    *   Original Foreground Color: `[Value]`
    *   Original Background Color: `[Value]`
    *   Calculated Contrast Ratio: `[Ratio]`
    *   WCAG 2.1 Compliance for `{{target_wcag_level}}`: `[Pass/Fail]`
2.  **Recommended Fixes (if necessary):**
    *   Proposed Foreground Color: `[New Value]` (e*g., a darker shade of current foreground or a new color)
    *   Proposed Background Color: `[New Value]` (e.g., a lighter shade of current background or a new color)
    *   Calculated Contrast Ratio (Proposed): `[New Ratio]`
    *   WCAG 2.1 Compliance for `{{target_wcag_level}}` (Proposed): `[Pass/Fail]`
    *   Justification: Explain the color adjustment strategy.

## Tips

This prompt is excellent for ensuring basic accessibility compliance for visual elements. It's straightforward and provides direct, measurable solutions for color contrast issues.
