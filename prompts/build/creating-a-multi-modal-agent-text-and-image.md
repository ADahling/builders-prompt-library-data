---
title: "Creating a Multi-Modal Agent (Text and Image)"
slug: creating-a-multi-modal-agent-text-and-image
stage: Build
category: "AI Agent Development"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-multi-modal-agent-text-and-image
---
# Creating a Multi-Modal Agent (Text and Image)

Get a Python script that encodes a local image, sends it with a question to OpenAI's vision API, and prints the model's description.

Variables: image_path

## Prompt

Build a multi-modal agent that can understand both text and images. You will use a vision-capable model like GPT-5 or Gemini 3 to describe an image.

**The Task:**

The agent should be able to take an image and a text prompt and answer a question about the image.

**Implementation (using OpenAI's API):**

1.  **Image Input:** The image needs to be provided to the API, usually as a base64-encoded string or a URL.
2.  **The Prompt:** The prompt will be a list of content blocks, not a single string.
    *   One block will be of type `text` containing the user's question (e.g., "What is the main subject of this image?").
    *   The other block will be of type `image_url` containing the image data.
3.  **The API Call:**
    *   Use the `openai.chat.completions.create` method.
    *   Pass the multi-part prompt to the `messages` parameter.
    *   Specify a vision-capable model, like `gpt-5`.

**Your Task:**

Write a Python script that:
1.  Loads an image from a local file (`{{image_path}}`).
2.  Encodes it in base64.
3.  Constructs the multi-modal prompt.
4.  Calls the OpenAI API.
5.  Prints the model's description of the image.

**Output:**

A Python script that demonstrates how to send an image and a question to a multi-modal LLM.
