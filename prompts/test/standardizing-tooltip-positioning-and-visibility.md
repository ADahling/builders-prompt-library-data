---
title: "Standardizing Tooltip Positioning and Visibility"
slug: standardizing-tooltip-positioning-and-visibility
stage: Test
category: "UX/UI Fixes"
grade: B
score: 74
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/standardizing-tooltip-positioning-and-visibility
---
# Standardizing Tooltip Positioning and Visibility

Get CSS and JavaScript guidance for inconsistent tooltips, covering dynamic placement, viewport edges, stacking, transitions, and accessibility.

Variables: component_1, component_2

## Prompt

Our application has various tooltips implemented across different components, such as '{{component_1}}' and '{{component_2}}'. The current tooltip behavior is inconsistent; some tooltips clip off-screen, others overlap critical UI elements, and their positioning isn't always optimal for readability. Your objective is to provide a set of best practices and specific CSS/JavaScript adjustments to standardize tooltip positioning and ensure consistent, non-obtrusive visibility.

Analyze the general requirements for tooltips in our application, considering their context (e.g., form fields, icon buttons, data visualizations). Propose a unified strategy for tooltip placement that dynamically adjusts to prevent viewport clipping and overlapping other interactive elements. This might involve using libraries like Popper.js or implementing custom logic with JavaScript to calculate optimal positions (top, bottom, left, right, or auto-placement). Detail how to handle scenarios where a tooltip might open near the edge of the screen.

Provide recommendations for CSS properties to control tooltip appearance, transition effects for smooth showing/hiding, and `z-index` management to ensure tooltips always appear above their associated elements and other content. Include guidance on ensuring tooltips are accessible for keyboard and screen reader users (e.g., using `aria-describedby` or similar). Your output should be a concise guide with actionable CSS and conceptual JavaScript strategies.

## Tips

This prompt focuses on practical solutions for common tooltip display issues, improving consistency and user experience across an application.
