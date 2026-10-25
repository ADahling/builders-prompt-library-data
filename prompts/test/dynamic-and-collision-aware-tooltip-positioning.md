---
title: "Dynamic and Collision-Aware Tooltip Positioning"
slug: dynamic-and-collision-aware-tooltip-positioning
stage: Test
category: "UX/UI Fixes"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/dynamic-and-collision-aware-tooltip-positioning
---
# Dynamic and Collision-Aware Tooltip Positioning

Implement collision-aware tooltip positioning using dynamic logic or libraries to ensure visibility and viewport containment.

Variables: tooltip_element, current_positioning_logic, problem_description, trigger_element, container_constraints

## Prompt

You are an advanced front-end developer tasked with implementing a robust and dynamic positioning system for a '{{tooltip_element}}' component. The current positioning logic, described as '{{current_positioning_logic}}', is causing issues like '{{problem_description}}', where the tooltip frequently overflows the viewport or is obscured by other elements, especially when triggered by '{{trigger_element}}' near the edges of its '{{container_constraints}}'. Your goal is to create a positioning solution that automatically adjusts the tooltip's placement to remain within the viewport and avoid collisions.

Describe the current tooltip's HTML structure and CSS, along with the trigger element. Detail the exact scenarios where the positioning fails. Your solution should involve a dynamic positioning strategy, potentially leveraging a library like Popper.js or Floating UI, or implementing a custom collision detection algorithm. Outline the logic for determining the optimal placement (e.g., `top`, `bottom`, `left`, `right`) and how to handle viewport boundaries. If using a library, specify the configuration and relevant methods. If custom, describe the JavaScript calculations required (e.g., `getBoundingClientRect()`, viewport dimensions) and the CSS adjustments. Consider adding an optional 'arrow' element that points to the trigger and also repositions dynamically. The output should include the current setup, a detailed explanation of the positioning problem, the proposed technical solution (CSS and JavaScript logic/library usage), and how it addresses viewport collisions and dynamic placement.

## Tips

This advanced prompt delves into complex UI positioning challenges, requiring knowledge of geometry, DOM manipulation, and potentially external libraries for robust solutions to avoid element overlap and viewport overflow.
