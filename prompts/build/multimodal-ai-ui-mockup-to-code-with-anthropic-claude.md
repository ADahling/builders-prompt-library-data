---
title: "Multimodal AI: UI Mockup to Code with Anthropic Claude"
slug: multimodal-ai-ui-mockup-to-code-with-anthropic-claude
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-ui-mockup-to-code-with-anthropic-claude
---
# Multimodal AI: UI Mockup to Code with Anthropic Claude

Automate the conversion of UI mockup images into responsive HTML and Tailwind CSS code using a Python script and the Claude Sonnet 5 API.

## Prompt

As a frontend developer, you want to speed up your workflow by converting hand-drawn wireframes or UI mockups directly into HTML/CSS code. You will use Anthropic's Claude Sonnet 5 for this.

Your task is to write a Python script that sends an image of a UI mockup to Claude and asks it to generate the corresponding frontend code.

**Scenario:**
- **Image:** Assume a local file named `login_mockup.png` showing a simple login form with an email field, password field, and a "Sign In" button.
- **Goal:** Generate clean, responsive HTML and Tailwind CSS code.

**Technical Requirements:**
- Use the 'anthropic' Python SDK.
- Read and base64-encode the `login_mockup.png` file.
- Construct the `messages` payload with the image block and a text block.
- The text prompt should instruct Claude to act as an expert frontend developer. It should ask for a single HTML file containing the structure and inline Tailwind CSS classes to replicate the design in the image.
- Instruct Claude to output *only* the HTML code block, without any markdown formatting backticks or conversational filler.
- Print the generated HTML code to the console.

**Output Format:**
A complete Python script. Include a comment that the user needs a `login_mockup.png` file.
