---
title: "WCAG Color Contrast Analysis and Fixes"
slug: wcag-color-contrast-analysis-and-fixes
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/wcag-color-contrast-analysis-and-fixes
---
# WCAG Color Contrast Analysis and Fixes

Audit UI color schemes for WCAG compliance and obtain specific hex-code recommendations to fix contrast issues for text and components.

Variables: component_description, background_color, text_color, interactive_element_color

## Prompt

You are a UI/UX accessibility expert. Your task is to analyze the color contrast of a specified UI component and provide actionable recommendations to achieve WCAG 2.1 AA or AAA compliance. Focus on text contrast against its background and the contrast of interactive elements. I will provide details about the component's current color scheme. Please identify any issues and propose specific color changes (using hex codes) that meet the target compliance level, explaining your rationale for each adjustment. Consider both normal text and large text requirements.

Component Description: {{component_description}}
Background Color (Hex): {{background_color}}
Primary Text Color (Hex): {{text_color}}
Interactive Element Color (Hex, if applicable): {{interactive_element_color}}

Your output should be structured as follows:
1.  **Current Contrast Ratios:** List the calculated contrast ratios for text/background and interactive elements/background.
2.  **Compliance Status:** State whether the current ratios meet WCAG 2.1 AA and AAA for normal and large text.
3.  **Recommendations:** For each non-compliant area, propose new hex codes for the foreground or background that achieve compliance. Provide at least two compliant options if possible. Explain why these new colors work and how they improve accessibility. If an interactive element's contrast is problematic, suggest a new color for it or its surrounding context.
4.  **Summary:** A brief summary of the most critical changes required.

## Tips

This prompt helps developers quickly identify and rectify color contrast issues, ensuring their UI is accessible to users with visual impairments. It's a fundamental accessibility check.
