---
title: "Testing for Missing Alt Text"
slug: testing-for-missing-alt-text
stage: Secure
category: "Accessibility (WCAG)"
grade: C
score: 68
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/testing-for-missing-alt-text
---
# Testing for Missing Alt Text

Write a webpage image-checking script that logs sources for images missing alt attributes and suggests adding appropriate alt text.

## Prompt

Write a script that scans through all images on a webpage to check for missing alt attributes. For each image without an alt attribute, log its src and suggest adding appropriate alt text. Use 'const images = document.querySelectorAll('img'); images.forEach((img) => { ... });'.

## Tips

This helps identify accessibility issues related to images.
