---
title: "Rectifying Dark Mode Inconsistencies and Contrast Issues"
slug: rectifying-dark-mode-inconsistencies-and-contrast-issues
stage: Test
category: "UX/UI Fixes"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/rectifying-dark-mode-inconsistencies-and-contrast-issues
---
# Rectifying Dark Mode Inconsistencies and Contrast Issues

Audit dark mode pages and get a CSS adjustment plan for contrast, unthemed elements, images, icons, and third-party components.

Variables: settings_page, profile_page, styling_framework

## Prompt

Our application supports a dark mode, but users have reported numerous inconsistencies on the '{{settings_page}}' and '{{profile_page}}' pages. These issues include poor color contrast for text and icons, overlooked elements remaining light-themed, and images with light backgrounds appearing jarringly out of place. Your task is to systematically analyze these pages and provide a detailed plan to rectify all dark mode inconsistencies and ensure optimal contrast and visual harmony.

Conduct a thorough audit of the specified pages in dark mode. Identify all UI elements that exhibit incorrect styling, insufficient contrast (against WCAG AA or AAA guidelines), or are not properly themed. This includes text, icons, buttons, input fields, borders, shadows, and background colors. Pay special attention to SVG icons and images that might not adapt well. For images, suggest strategies like using `prefers-color-scheme` in CSS for different image sources or overlaying subtle dark layers.

Your plan should detail specific CSS variables, properties, and selectors that need adjustment. For color contrast, recommend a new color palette for dark mode that ensures readability and accessibility. Provide a systematic approach for updating overlooked elements. Include considerations for dynamic content or third-party components that might not natively support dark mode. The output should be a structured report outlining identified issues, proposed CSS/SCSS solutions with code examples, and a checklist for maintaining dark mode consistency across the entire application, specifically for `{{styling_framework}}`.

## Tips

This advanced prompt helps developers systematically identify and fix dark mode issues, ensuring a consistent, accessible, and visually pleasing experience.
