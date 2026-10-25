---
title: "Image Generation: Creating Images with Stable Diffusion API"
slug: image-generation-creating-images-with-stable-diffusion-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/image-generation-creating-images-with-stable-diffusion-api
---
# Image Generation: Creating Images with Stable Diffusion API

Generate a Python script that integrates the Stability AI API to create and save fantasy concept art from a text prompt.

## Prompt

You are a game developer creating assets for a fantasy-themed game. You need to generate a concept art piece for a magical sword using the Stability AI API (Stable Diffusion).

Your task is to write a Python script that sends a text prompt to the Stability AI API to generate an image.

**Image Concept:**
"A glowing, ethereal sword made of crystal, embedded in a stone altar in the middle of an ancient, moss-covered forest. The style should be epic fantasy digital painting."

**Technical Requirements:**
- Use the 'requests' library to make a POST request to the Stability AI API endpoint for a specific model (e.g., Stable Diffusion 3).
- Your script must handle authentication by sending your Stability AI API key in the 'Authorization' header. The key should be retrieved from an environment variable 'STABILITY_API_KEY'.
- The request body should be a JSON payload containing the 'prompt', and other parameters like 'aspect_ratio' ('1:1').
- The API will return the image data directly. Your script must save this binary data to a file named 'generated_sword.png'.
- After saving the file, the script should print a confirmation message like "Image saved to generated_sword.png".
- You will need to consult the Stability AI API documentation for the exact endpoint URL and request payload structure.

**Output Format:**
A complete Python script that generates an image and saves it locally.
