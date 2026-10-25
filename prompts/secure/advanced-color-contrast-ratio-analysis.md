---
title: "Advanced Color Contrast Ratio Analysis"
slug: advanced-color-contrast-ratio-analysis
stage: Secure
category: "Accessibility (WCAG)"
grade: A+
score: 98
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-color-contrast-ratio-analysis
---
# Advanced Color Contrast Ratio Analysis

Calculate color contrast ratios against WCAG 2.1 standards and receive accessible color pairing alternatives to ensure web readability.

Variables: text_color, background_color, minimum_contrast_ratio

## Prompt

As a developer working on enhancing the accessibility of your web application, ensure that the color contrast ratios between text and background colors meet the WCAG 2.1 standards. This ensures readability for users with visual impairments. 

Please provide the following details: 
- The hex code of the text color: {{text_color}} 
- The hex code of the background color: {{background_color}} 
- The minimum acceptable contrast ratio (e.g., 4.5:1 for normal text, 3:1 for large text): {{minimum_contrast_ratio}} 

Your task is to calculate the contrast ratio between the provided colors and evaluate if it meets the specified minimum standard. If the contrast ratio is below the specified threshold, suggest alternative colors that would improve accessibility while maintaining the design intent. The output should include: 
1. Calculated contrast ratio. 
2. Compliance status (Pass/Fail) based on the specified standard. 
3. Suggested alternative text and background color combinations if the compliance status is 'Fail'. 

Adhere to the following format for the output:
{
  "contrast_ratio": "calculated value",
  "compliance_status": "Pass/Fail",
  "suggested_colors": [
    { "text_color": "#xxxxxx", "background_color": "#xxxxxx" },
    ...
  ]
}

Ensure that the suggested colors maintain aesthetic harmony with the original design.

## Tips

Use this prompt when you need to verify or improve the contrast ratios of color combinations in a web project to ensure accessibility compliance. It will calculate the current contrast ratio, check against the minimum standard, and suggest alternatives if necessary.
