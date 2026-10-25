---
title: "Multimodal AI: Image Analysis with Anthropic Claude 3"
slug: multimodal-ai-image-analysis-with-anthropic-claude-3
stage: Build
category: "LLM & AI Integration"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-image-analysis-with-anthropic-claude-3
---
# Multimodal AI: Image Analysis with Anthropic Claude 3

Implement a Python script using the Anthropic API to generate descriptive alt-text from local images via base64 encoding and the latest Claude.

## Prompt

You are building an accessibility tool that describes images for visually impaired users. You've chosen Anthropic's Claude Sonnet 5 for its strong multimodal capabilities.

Your task is to write a Python script that sends a local image file to the Claude Sonnet 5 model and asks it to generate a concise and helpful 'alt text' description for the image.

**Scenario:**
- **Image:** A local image file named 'chart.png', which contains a simple bar chart showing monthly sales data.
- **Prompt:** "Generate a concise and descriptive alt text for this image. The alt text should accurately describe the chart's content for someone who cannot see it."

**Technical Requirements:**
- Use the 'anthropic' and 'base64' libraries.
- The script must read the local image file ('chart.png') in binary mode.
- It must then encode the image data into a base64 string.
- You'll also need to determine the media type (e.g., 'image/png').
- The `messages` payload for the Claude API call must contain a content block for the text prompt and another content block for the image. The image block must include the `type` ('image'), and a `source` dictionary containing the `type` ('base64'), `media_type`
