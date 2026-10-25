---
title: "Optimize Tooltip Positioning for Visibility and UX"
slug: optimize-tooltip-positioning-for-visibility-and-ux
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-tooltip-positioning-for-visibility-and-ux
---
# Optimize Tooltip Positioning for Visibility and UX

Generate dynamic, collision-aware tooltip positioning strategies using CSS and JavaScript to ensure optimal visibility and accessibility.

Variables: trigger_element_location, tooltip_content_length, viewport_dimensions

## Prompt

As a UI/UX specialist, your goal is to suggest optimal positioning strategies for a tooltip given its trigger element's location, the tooltip's content length, and the available viewport space. The objective is to ensure the tooltip is always fully visible, does not obscure critical UI elements, and maintains a clear association with its trigger. Consider edge cases where the trigger is near the viewport edges, and propose a robust positioning logic that can adapt dynamically. Provide CSS-based solutions where possible, and outline JavaScript fallback logic for more complex scenarios.

**Trigger Element Location (relative to viewport):** `{{trigger_element_location}}` (e.g., 'Top-left corner', 'Center of screen', 'Near bottom-right edge')
**Tooltip Content Length:** `{{tooltip_content_length}}` (e.g., 'Short, single line of text', 'Medium, 2-3 lines of text', 'Long paragraph')
**Viewport Dimensions (width x height in px):** `{{viewport_dimensions}}` (e.g., '1920x1080', '375x667 (mobile)')

**Output Format:** Provide a structured recommendation with the following sections:
1.  **Current Positioning Challenges:** Briefly describe potential issues with static tooltip positioning in the given context.
2.  **Primary Positioning Strategy (CSS-first):**
    *   **Preferred Position:** Suggest an initial default position (e.g., 'above', 'below', 'left', 'right').
    *   **CSS Properties:** Outline relevant CSS for basic positioning (e.g., `position: absolute`, `top`, `left`, `transform`, `pointer-events`).
3.  **Dynamic Adjustment Logic (JavaScript-assisted):**
    *   **Edge Case Handling:** Describe how to detect and respond to viewport boundary collisions.
    *   **Fallback Positions:** Suggest alternative positions if the primary one is not feasible.
    *   **Pseudocode/Logic Flow:** Provide a high-level pseudocode or logical steps for dynamic positioning.
4.  **Accessibility Considerations:** Briefly mention ARIA attributes for tooltips.
5.  **Code Snippet Example (CSS/JS concepts):** A basic demonstration of the proposed approach.

## Tips

This prompt addresses a common UI annoyance: tooltips obscuring content or going off-screen. It provides practical solutions for dynamic and user-friendly tooltip placement.
