---
title: "Image Generation: Creating Images with OpenAI DALL-E 3"
slug: image-generation-creating-images-with-openai-dall-e-3
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/image-generation-creating-images-with-openai-dall-e-3
---
# Image Generation: Creating Images with OpenAI DALL-E 3

Generate a high-quality steampunk fox image by writing a Python script that integrates the OpenAI DALL-E 3 API to produce a specific URL.

## Prompt

As a creative director for a marketing campaign, you need to generate a unique and high-quality image based on a detailed concept. You will use OpenAI's DALL-E 3 model for this task.

Your task is to write a Python script that calls the OpenAI Images API to generate an image.

**Image Concept:**
"A photorealistic image of a majestic red fox wearing a tiny, vintage aviator helmet, sitting in the cockpit of a steampunk-inspired flying machine made of brass and wood. The background is a beautiful sunset over a mountain range."

**Technical Requirements:**
- Use the 'openai' Python library.
- Use the 'dall-e-3' model.
- The script should make a call to `client.images.generate()`.
- Specify the prompt with the detailed image concept.
- Request a single image ('n=1').
- Set the image size to '1024x1024'.
- Set the quality to 'hd' for a more detailed image.
- The API response will contain a URL for the generated image. Your script must extract this URL and print it to the console.

**Output Format:**
A complete Python script that, when run, prints the URL of the newly generated image.
