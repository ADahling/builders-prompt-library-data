---
title: "Image Generation: Inpainting with DALL-E 2 or SDXL"
slug: image-generation-inpainting-with-dall-e-2-or-sdxl
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/image-generation-inpainting-with-dall-e-2-or-sdxl
---
# Image Generation: Inpainting with DALL-E 2 or SDXL

Generate a Python script to perform AI-driven image inpainting using the DALL-E 2 or Stability AI API to seamlessly replace masked objects.

## Prompt

You are a photo editor using AI to modify an existing image. You need to remove an unwanted object from a photo and have the AI fill in the background seamlessly. This process is called 'inpainting'.

Your task is to write a Python script that demonstrates how to perform inpainting using an AI image generation API (like OpenAI's DALL-E 2 or a Stability AI model that supports it).

**Scenario:**
- **Image:** You have a local image file named 'photo.png'.
- **Mask:** You have a second image file, 'mask.png', of the same dimensions. This mask is all black except for a white area covering the object you want to remove.
- **Prompt:** A text description of what should be filled into the masked area, e.g., "a grassy field with blue sky".

**Technical Requirements (using OpenAI DALL-E 2 as an example):**
- Use the 'openai' Python library.
- The script must open both 'photo.png' and 'mask.png' in binary read mode.
- Make a call to the `client.images.edit()` method (this is the inpainting endpoint for DALL-E 2).
- Pass the image file, the mask file, and the text prompt.
- Specify the number of images to generate and the desired size.
- The API will return a URL to the newly generated, edited image. Your script should print this URL.

**Output Format:**
A complete Python script demonstrating the inpainting process. Include comments explaining that the user needs to provide their own 'photo.png' and 'mask.png' files.
