---
title: "Analyze and Improve Color Contrast Ratios for Accessibility Compliance"
slug: analyze-and-improve-color-contrast-ratios-for-accessibility-compliance
stage: Secure
category: "Accessibility (WCAG)"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/analyze-and-improve-color-contrast-ratios-for-accessibility-compliance
---
# Analyze and Improve Color Contrast Ratios for Accessibility Compliance

Evaluate hex codes for WCAG 2.1 contrast compliance and generate accessible color alternatives to ensure web readability and inclusivity.

Variables: text_color, background_color

## Prompt

You are tasked with evaluating and improving the color contrast ratios for a web application to ensure it meets accessibility standards. The goal is to achieve compliance with the Web Content Accessibility Guidelines (WCAG) 2.1, specifically focusing on color contrast requirements. 

Instructions:

1. **Input Details:** Provide the color codes and background colors currently used in the application. Include both text and background colors as follows:
   - Text Color: {{text_color}}
   - Background Color: {{background_color}}

2. **Contrast Ratio Calculation:** Calculate the contrast ratio between the text and background colors. Use the formula provided by WCAG 2.1 to determine the contrast ratio.

3. **Compliance Check:** Determine if the current contrast ratio meets the minimum requirements for WCAG 2.1 compliance:
   - A minimum of 4.5:1 for regular text.
   - A minimum of 3:1 for large text (18pt and larger, or 14pt bold and larger).

4. **Improvement Suggestions:** If the current contrast ratio does not meet the compliance standards, suggest alternative color combinations that would achieve the required contrast without compromising the application's design aesthetics. Provide at least two alternative color combinations for each non-compliant pair.

Output Format:
- Calculate and display the current contrast ratio.
- Indicate whether it is compliant or non-compliant with WCAG 2.1.
- List suggestions for alternative color combinations, if necessary.

This task is critical for ensuring accessibility and inclusivity of your web application. The output should guide designers and developers in making informed decisions to enhance usability for all users.

## Tips

Use this prompt when you need to assess and improve the color contrast of text elements on a web application to ensure accessibility compliance. Ideal for developers and designers working towards WCAG 2.1 standards.
