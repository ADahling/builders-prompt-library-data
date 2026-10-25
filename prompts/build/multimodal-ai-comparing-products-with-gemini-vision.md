---
title: "Multimodal AI: Comparing Products with Gemini Vision"
slug: multimodal-ai-comparing-products-with-gemini-vision
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-comparing-products-with-gemini-vision
---
# Multimodal AI: Comparing Products with Gemini Vision

Develop a Python script using Gemini 3 to perform multimodal visual comparisons between two local product images.

## Prompt

You are building a feature for an e-commerce app that allows users to upload pictures of two different products and get an AI-powered comparison.

Your task is to write a Python script using the Google Gemini 3 model that takes two images and a prompt to compare them.

**Scenario:**
- **Image 1:** A local file named 'product_A.jpg' (e.g., a picture of a smartphone).
- **Image 2:** A local file named 'product_B.jpg' (e.g., a picture of a different smartphone).
- **Prompt:** "Compare these two products. Based on their visual appearance, list the key differences in design, size, and any visible features like cameras or ports."

**Technical Requirements:**
- Use the 'google-generativeai' and 'Pillow' libraries.
- The script must open both local image files.
- Use the 'gemini-3-latest' model.
- The content passed to `model.generate_content()` must be a list containing three items: the text prompt, the first image object, and the second image object.
- The script should then make the API call and print the model's comparative analysis to the console.
- Ensure your Google AI API key is handled securely.

**Output Format:**
A complete Python script. Include a comment that the user needs to provide 'product_A.jpg' and 'product_B.jpg' for the script to work.
