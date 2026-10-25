---
title: "Implement Advanced Custom Scroll Behavior"
slug: implement-advanced-custom-scroll-behavior
stage: Test
category: "UX/UI Fixes"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-advanced-custom-scroll-behavior
---
# Implement Advanced Custom Scroll Behavior

Get an HTML, CSS, and JavaScript plan for custom scrolling in your app, with performance, browser compatibility, and accessibility considerations.

Variables: target_scroll_behavior, scroll_area_description, tech_stack

## Prompt

You need to implement a sophisticated custom scroll behavior for a specific section of a web application, moving beyond default browser scrolling. This could involve features like smooth scrolling to anchors, sticky headers/footers that adapt on scroll, parallax effects, or infinite scrolling with dynamic content loading. Your task is to design and provide a technical implementation plan, including relevant HTML structure, CSS properties, and JavaScript logic, for the specified custom scroll behavior. Focus on performance optimization (e.g., debouncing scroll events, using `requestAnimationFrame`), cross-browser compatibility, and accessibility considerations (e.g., keyboard navigation, reduced motion preferences). Explain the core logic and how it addresses the desired user experience.

**Target Scroll Behavior:** {{target_scroll_behavior}} (e.g., 'sticky header that shrinks on scroll', 'smooth scroll to anchor links with offset', 'infinite scroll for a content feed')
**Scroll Area Description/Context:** {{scroll_area_description}} (e.g., 'main content feed with dynamic articles', 'single-page application navigation')
**Current Tech Stack:** {{tech_stack}} (e.g., React, Vue, vanilla JS)

**Output Format:** Provide a 'Conceptual Overview', 'HTML Structure Recommendations', 'CSS Styling (with key properties)', and 'JavaScript Logic (pseudo-code or specific API calls)'. Detail how performance and accessibility are handled.

## Tips

This advanced prompt guides developers in implementing complex, performant, and accessible custom scroll behaviors, crucial for modern web experiences.
