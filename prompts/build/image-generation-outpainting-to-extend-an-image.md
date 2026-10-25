---
title: "Image Generation: Outpainting to Extend an Image"
slug: image-generation-outpainting-to-extend-an-image
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/image-generation-outpainting-to-extend-an-image
---
# Image Generation: Outpainting to Extend an Image

Develop a Python script using Pillow and the DALL-E API to programmatically extend image boundaries through automated outpainting.

## Prompt

You are a graphic designer with an image that you wish was wider. You want to use AI to extend the image's canvas and generate new content that seamlessly blends with the original. This process is called 'outpainting'.

Your task is to design the logic and write a Python script that uses an AI image API (like DALL-E 2) to perform outpainting.

**Scenario:**
- **Original Image:** A square image (e.g., 1024x1024) of a portrait.
- **Goal:** Extend the image to the left and right to create a landscape-oriented image (e.g., 1792x1024).

**Technical Requirements (using DALL-E 2 as an example):**
- **Image Preparation:** The key to outpainting is to create a new, larger transparent canvas and place your original image in the middle.
    -   Use the 'Pillow' (PIL) library to create a new RGBA image of the target dimensions (e.g., 1792x1024).
    -   Paste your original square image into the center of this new transparent canvas.
    -   Save this new image as 'prepared_for_outpainting.png'.
- **Mask Creation:** You also need to create a mask that tells the AI which parts of the new image are transparent and need to be filled in.
    -   Create another RGBA image of the target dimensions, completely transparent.
    -   Save this as 'outpainting_mask.png'.
- **API Call:**
    -   Use the `client.images.edit()` method.
    -   The 'image' parameter is your 'prepared_for_outpainting.png'.
    -   The 'mask' parameter is your 'outpainting_mask.png'.
    -   The 'prompt' should describe the entire desired scene, e.g., "A portrait of a person standing in a field of flowers."
- **Output:** Print the URL of the resulting wide-screen image.

**Output Format:**
A complete Python script demonstrating the image preparation and API call for outpainting.
