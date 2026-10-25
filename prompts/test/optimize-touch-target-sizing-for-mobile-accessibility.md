---
title: "Optimize Touch Target Sizing for Mobile Accessibility"
slug: optimize-touch-target-sizing-for-mobile-accessibility
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-touch-target-sizing-for-mobile-accessibility
---
# Optimize Touch Target Sizing for Mobile Accessibility

Audit UI elements to ensure WCAG-compliant touch target sizes and spacing for improved mobile accessibility and tap accuracy.

Variables: ui_element_description, current_dimensions, target_platform

## Prompt

As a mobile UX designer and accessibility expert, evaluate the provided descriptions of UI elements and their current dimensions. Your objective is to recommend optimal touch target sizes and necessary spacing adjustments to ensure compliance with WCAG 2.1 guidelines (specifically Success Criterion 2.5.5: Target Size) and general mobile usability best practices. The goal is to prevent accidental taps, improve user interaction on touchscreens, and enhance accessibility for users with motor impairments. Provide specific pixel values for minimum touch targets and suggested padding/margin adjustments.

**UI Element Description:** `{{ui_element_description}}` (e.g., 'A primary call-to-action button', 'A list of navigation links', 'A small icon button within a toolbar')
**Current Dimensions (width x height in px):** `{{current_dimensions}}` (e.g., '30px x 30px', 'Text link with 10px line-height')
**Target Platform:** `{{target_platform}}` (e.g., 'iOS and Android mobile devices', 'Tablet devices')

**Output Format:** Provide a structured recommendation with the following sections:
1.  **Current State Analysis:** Briefly summarize the current element's touch target adequacy.
2.  **WCAG 2.1 Target Size Reference:** State the minimum recommended touch target size (e.g., 44x44 CSS pixels).
3.  **Recommended Touch Target:**
    *   **Minimum Recommended Size:** `[Width]px x [Height]px`
    *   **Proposed Implementation Strategy:** Suggest how to achieve this (e.g., 'Increase padding', 'Adjust minimum width/height CSS properties', 'Use pseudo-elements').
4.  **Spacing Recommendations:** Advise on optimal spacing (margins/padding) around the element to further improve tap accuracy and prevent adjacent element interference.
5.  **Code Snippet Example (CSS):** Provide a basic CSS example demonstrating how to apply the recommendations.

## Tips

This prompt is crucial for mobile-first development, ensuring that interactive elements are easily tappable for all users. It translates accessibility guidelines into practical CSS adjustments.
