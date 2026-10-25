---
title: "Generate Descriptive Alt Text for Images"
slug: generate-descriptive-alt-text-for-images
stage: Secure
category: "Accessibility (WCAG)"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-descriptive-alt-text-for-images
---
# Generate Descriptive Alt Text for Images

Generate accessible, screen-reader-friendly image alt text in JSON format following standard web accessibility and character limit guidelines.

Variables: project_name, image_descriptions

## Prompt

You are tasked with creating descriptive alt text for images used in the {{project_name}} project. The purpose of alt text is to improve accessibility by providing a textual alternative to visual content. Follow these guidelines to generate effective alt text: 1. Describe the image content clearly and concisely, focusing on the main subjects and relevant details. 2. Avoid phrases like 'image of' or 'picture of' as this is implicit in the context. 3. If the image includes text, transcribe the text unless it is overly extensive. 4. Consider the context in which the image is used to ensure the alt text complements the surrounding content. 5. Keep the description concise, ideally under 125 characters, to ensure compatibility with screen readers. 6. Use correct spelling and grammar to maintain professionalism. Provide alt text for the following images: {{image_descriptions}}. Return the alt text in a JSON format with each image key paired with its alt text.

## Tips

Use this prompt when you need to create alt text for images to ensure accessibility compliance. This is particularly useful during the development of websites or applications that include visual content. The prompt guides you on how to write alt text that is both informative and concise, enhancing the experience for users relying on screen readers.
