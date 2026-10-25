---
title: "Achieving WCAG Compliant Color Contrast for UI Elements"
slug: achieving-wcag-compliant-color-contrast-for-ui-elements
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/achieving-wcag-compliant-color-contrast-for-ui-elements
---
# Achieving WCAG Compliant Color Contrast for UI Elements

Generate WCAG-compliant color pairs for UI elements to ensure accessibility standards are met while preserving visual design consistency.

Variables: element_type, current_foreground_color, current_background_color, wcag_level

## Prompt

You are a front-end developer responsible for ensuring the accessibility of a web application. A specific UI element, described as '{{element_type}}', currently uses a foreground color of '{{current_foreground_color}}' against a background color of '{{current_background_color}}'. This combination has been identified as failing to meet the WCAG '{{wcag_level}}' color contrast ratio requirements, making it difficult for users with visual impairments to read or perceive. Your task is to propose new color values that meet or exceed the specified WCAG level while maintaining the overall aesthetic of the application.

Provide the current hexadecimal or RGB values for both the foreground and background colors. Explain the WCAG contrast ratio requirement for '{{wcag_level}}' and why the current combination fails. Using a systematic approach, suggest at least two alternative color pairs (new foreground and/or background colors) that achieve the required contrast ratio. For each suggestion, provide the new color values (hexadecimal is preferred) and explicitly state the calculated contrast ratio, confirming it meets the '{{wcag_level}}' standard. Additionally, briefly explain your methodology for selecting these new colors, considering factors like brand guidelines or existing color palettes. The output should clearly state the original problem, the WCAG requirement, and the proposed compliant color solutions with their respective contrast ratios.

## Tips

This beginner-level prompt introduces developers to fundamental web accessibility principles, specifically WCAG color contrast guidelines, and provides a practical exercise in applying them.
