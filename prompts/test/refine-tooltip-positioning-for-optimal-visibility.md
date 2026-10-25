---
title: "Refine Tooltip Positioning for Optimal Visibility"
slug: refine-tooltip-positioning-for-optimal-visibility
stage: Test
category: "UX/UI Fixes"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/refine-tooltip-positioning-for-optimal-visibility
---
# Refine Tooltip Positioning for Optimal Visibility

Implement dynamic CSS positioning to prevent tooltip overflow and ensure optimal visibility relative to trigger elements and viewport boundaries.

Variables: tooltip_html_structure, tooltip_css_styles, viewport_constraints

## Prompt

You are a senior front-end developer tasked with resolving a common UX issue: tooltips that are either cut off by the viewport, overlap crucial UI elements, or appear in inconvenient locations. Your goal is to provide a robust CSS solution for a tooltip component to ensure it always appears clearly and effectively. The tooltip should adapt its position based on available space around its trigger element, prioritizing top/bottom placement, then left/right, and finally adjusting to prevent viewport overflow. Consider scenarios where the trigger element is near the edge of the screen.

Input:
- `{{tooltip_html_structure}}`: The current HTML structure for the tooltip and its trigger.
- `{{tooltip_css_styles}}`: The existing CSS styles applied to the tooltip and its trigger.
- `{{viewport_constraints}}`: Any specific viewport dimensions or responsiveness requirements (e.g., 'mobile-first', 'desktop-only').

Instructions:
1. Analyze the provided HTML and CSS to understand the current tooltip implementation.
2. Propose modifications to the CSS to implement intelligent positioning. This should involve using `position: absolute`, `transform`, and possibly `top`/`bottom`/`left`/`right` properties.
3. Include a mechanism to detect and prevent viewport overflow, potentially by dynamically adjusting the tooltip's `transform-origin` or its `top`/`left` values.
4. Ensure the tooltip remains visually connected to its trigger element.
5. Provide a clear explanation of each CSS property change and why it addresses the positioning issue.

Output Format:
Provide the updated CSS code block, followed by a detailed explanation of the changes and how they achieve the desired adaptive positioning. If JavaScript is strictly necessary for advanced dynamic positioning, provide pseudocode outlining the logic.

## Tips

This prompt addresses a fundamental UX issue for interactive elements. The solution should focus primarily on CSS, but acknowledge JS for complex dynamic positioning.
