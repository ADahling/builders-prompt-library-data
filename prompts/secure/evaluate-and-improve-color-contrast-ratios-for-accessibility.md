---
title: "Evaluate and Improve Color Contrast Ratios for Accessibility"
slug: evaluate-and-improve-color-contrast-ratios-for-accessibility
stage: Secure
category: "Accessibility (WCAG)"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/evaluate-and-improve-color-contrast-ratios-for-accessibility
---
# Evaluate and Improve Color Contrast Ratios for Accessibility

Audit UI color pairs for WCAG 2.1 AA compliance and receive accessible color suggestions to enhance readability and inclusive design.

Variables: tech_stack

## Prompt

You are tasked with evaluating and improving the color contrast ratios of a web application to ensure compliance with accessibility standards. The application is built using {{tech_stack}} and presents several UI elements with varying text and background colors. Your goal is to identify any color contrast issues that do not meet the WCAG 2.1 AA standards, which require a minimum contrast ratio of 4.5:1 for normal text and 3:1 for large text. 

Please follow these instructions:

1. Analyze the provided list of color pairs in the application, each consisting of a foreground (text) color and a background color. You should calculate the contrast ratio for each pair.

2. Identify pairs that do not meet the required contrast ratio standards.

3. Suggest alternative colors that would satisfy the minimum contrast requirements while maintaining the application's overall aesthetic.

4. Format your output as a list of objects, each containing:
   - "element": Description or identifier of the UI element.
   - "current_foreground_color": The current text color in hexadecimal format.
   - "current_background_color": The current background color in hexadecimal format.
   - "current_contrast_ratio": The calculated contrast ratio.
   - "meets_standard": A boolean indicating if the current pair meets the WCAG 2.1 AA standards.
   - "suggested_foreground_color": An alternative text color in hexadecimal format that would meet the standards.

Here's an example of the expected format:
{
  "element": "header text",
  "current_foreground_color": "#000000",
  "current_background_color": "#ffffff",
  "current_contrast_ratio": "21:1",
  "meets_standard": true,
  "suggested_foreground_color": "#000000"
}

Use this prompt to ensure that your application is accessible to users with visual impairments, enhancing usability and compliance with accessibility guidelines.

## Tips

Use this prompt when you need to ensure your web application meets accessibility standards regarding color contrast ratios. It is especially useful during the design review or QA phase to identify and correct potential accessibility issues in your UI.
