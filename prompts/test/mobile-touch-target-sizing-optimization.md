---
title: "Mobile Touch Target Sizing Optimization"
slug: mobile-touch-target-sizing-optimization
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/mobile-touch-target-sizing-optimization
---
# Mobile Touch Target Sizing Optimization

Optimize mobile UI touch targets and spacing to ensure compliance with Apple, Google, and WCAG accessibility standards for better usability.

Variables: ui_description, interactive_elements_list

## Prompt

You are a mobile UX specialist. Your goal is to review the touch target sizes for interactive elements within a given mobile UI context and recommend adjustments to meet industry best practices (e.g., Apple's Human Interface Guidelines, Android's Material Design, WCAG 2.1 AA/AAA for pointer targets, generally 44x44 CSS pixels or larger). I will provide a description of the UI and a list of interactive elements with their current sizes. Identify any elements that are too small or too close together and suggest specific size increases or spacing adjustments. Explain how these changes improve usability for touch interactions.

UI Description: {{ui_description}}
Interactive Elements and Current Sizes (e.g., 'Button A: 32x32px', 'Icon B: 24x24px', 'Link C: 20px font-size with 8px padding'): {{interactive_elements_list}}.

Your output should include:
1.  **Analysis of Current State:** For each listed interactive element, state its current effective touch target size and whether it meets the recommended 44x44 CSS pixel minimum. Note any instances where elements are too close.
2.  **Specific Recommendations:** For each non-compliant element, propose a new minimum size (width and height in CSS pixels) and/or padding adjustments to ensure it meets the recommended touch target size. If elements are too close, suggest increased spacing (in CSS pixels) between them. Explain the rationale for each recommendation, emphasizing improved accuracy and comfort for touch users.
3.  **Implementation Guidance:** Offer general advice on how to implement these changes effectively in a responsive mobile layout.

## Tips

Crucial for mobile applications, this prompt helps ensure that interactive elements are large enough and spaced appropriately for easy and error-free touch interaction, improving overall usability.
