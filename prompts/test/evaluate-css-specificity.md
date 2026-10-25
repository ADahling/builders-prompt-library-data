---
title: "Evaluate CSS Specificity"
slug: evaluate-css-specificity
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 74
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/evaluate-css-specificity
---
# Evaluate CSS Specificity

Review stylesheets for high-specificity CSS selectors and get a list of instances with simpler alternatives to improve maintainability.

Variables: styles_directory

## Prompt

Examine the stylesheets in {{styles_directory}} for CSS selectors with high specificity. List these instances and suggest simpler selectors to reduce specificity and improve maintainability.

## Tips

Reducing specificity can make styles easier to override and maintain.
