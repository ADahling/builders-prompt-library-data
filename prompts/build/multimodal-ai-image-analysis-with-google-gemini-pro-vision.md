---
title: "Multimodal AI: Image Analysis with Google Gemini Pro Vision"
slug: multimodal-ai-image-analysis-with-google-gemini-pro-vision
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-image-analysis-with-google-gemini-pro-vision
---
# Multimodal AI: Image Analysis with Google Gemini Pro Vision

Generate a Python script to analyze a local image using the Gemini Pro Vision model and describe its visual contents via the Google AI SDK.

## Prompt

As a developer exploring multimodal AI capabilities, you want to use Google's Gemini Pro Vision model to analyze an image and describe its contents.

Your task is to create a Python script that uses the 'google-generativeai' library to send an image to the Gemini API and generate a textual description.

**Scenario:**
- **Image:** You will need to load a local image file. For this exercise, assume you have an image file named 'sample_image.jpg' in the same directory as your script. You can add a comment on how to create a placeholder image if needed.
- **Prompt:** "Describe this image in detail, focusing on the main subject and the background elements."

**Technical Requirements:**
- Use the 'google-generativeai' and 'Pillow' (PIL) libraries.
- The script must first open the local image file ('sample_image.jpg') using `Image.open()`.
- Use the 'gemini-pro-vision' model.
- The content passed to `model.generate_content()` must be a list containing both the text prompt and the opened image object.
- The script should then make the API call and print the `text` part of the model's response to the console.
- Ensure your Google AI API key is handled securely.

**Output Format:**
A complete Python script. Before running, the user would need a 'sample_image.jpg' file. You should add a comment to clarify this dependency.
