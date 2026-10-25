---
title: "Resolving Responsive Layout Breaks for a Component"
slug: resolving-responsive-layout-breaks-for-a-component
stage: Test
category: "UX/UI Fixes"
grade: A
score: 82
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolving-responsive-layout-breaks-for-a-component
---
# Resolving Responsive Layout Breaks for a Component

Fix responsive layout shifts and component breakage on small screens by generating optimized CSS media queries and flexible layout rules.

Variables: component_name, target_breakpoint, desired_layout_description

## Prompt

You are a front-end developer tasked with fixing a responsive layout issue for a specific UI component. The component, named '{{component_name}}', is experiencing layout breaks or undesirable visual shifts when viewed on screens smaller than {{target_breakpoint}} pixels. Your goal is to provide a detailed CSS solution, primarily using media queries, to ensure the component maintains an optimal and {{desired_layout_description}} layout across various screen sizes, especially below the specified breakpoint. 

Provide the complete current CSS for the '{{component_name}}' component, including any relevant parent container styles if they influence the layout. Explain the exact nature of the layout break (e.g., elements overlapping, text wrapping unexpectedly, incorrect alignment, horizontal scrolling). Based on this, propose a revised or additional CSS block within a media query that specifically targets screens at or below {{target_breakpoint}} pixels. The solution should be robust, avoid hardcoding pixel values where percentages or flexible units are more appropriate, and consider potential future responsiveness needs. Include comments in the CSS to explain the purpose of each new rule. The output should be a detailed explanation of the problem, the proposed CSS fixes, and a brief rationale for each change.

## Tips

This prompt helps developers address common responsive design issues by focusing on specific breakpoints and component-level adjustments using media queries. It's ideal for understanding fundamental responsive CSS techniques.
