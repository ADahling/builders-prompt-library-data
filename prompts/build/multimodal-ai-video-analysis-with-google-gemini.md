---
title: "Multimodal AI: Video Analysis with Google Gemini"
slug: multimodal-ai-video-analysis-with-google-gemini
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-video-analysis-with-google-gemini
---
# Multimodal AI: Video Analysis with Google Gemini

Automate video content moderation by uploading files to Gemini 3, polling for processing status, and extracting safety summaries.

## Prompt

You are building a content moderation system for a video sharing platform. You need to analyze uploaded videos to generate a brief summary and flag any potential policy violations. You will use Google's Gemini 3, which supports native video understanding.

Your task is to write a Python script that uploads a video file to the Gemini API and analyzes it.

**Scenario:**
- **Video:** Assume a local file named `sample_video.mp4`.
- **Prompt:** "Summarize the events in this video. Are there any scenes depicting violence or dangerous activities?"

**Technical Requirements:**
- Use the 'google-generativeai' Python library.
- You must first upload the video file using `genai.upload_file(path='sample_video.mp4')`.
- Video processing takes time. You must implement a `while` loop that checks the `file.state` and waits until it is `ACTIVE` before proceeding. Use `time.sleep()` to avoid spamming the API.
- Once active, call `model.generate_content()` passing a list containing the uploaded file object and your text prompt.
- Print the model's analysis to the console.
- Finally, clean up by deleting the uploaded file using `genai.delete_file(file.name)`.

**Output Format:**
A complete Python script demonstrating the video upload, polling, analysis, and cleanup process.
