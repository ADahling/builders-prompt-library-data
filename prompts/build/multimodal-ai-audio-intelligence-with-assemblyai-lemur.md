---
title: "Multimodal AI: Audio Intelligence with AssemblyAI LeMUR"
slug: multimodal-ai-audio-intelligence-with-assemblyai-lemur
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-audio-intelligence-with-assemblyai-lemur
---
# Multimodal AI: Audio Intelligence with AssemblyAI LeMUR

Implement a Python script using the AssemblyAI SDK to transcribe business audio and generate high-quality summaries with the LeMUR framework.

## Prompt

You are building a tool for market researchers to analyze earnings calls. You need to go beyond simple transcription and extract summaries, key topics, and action items from the audio. You will use AssemblyAI's LeMUR (Language Models for Understanding Recordings) framework.

Your task is to write a Python script that first transcribes an audio file and then uses LeMUR to generate a summary.

**Scenario:**
- **Audio URL:** A publicly accessible URL of an earnings call or a similar business meeting.

**Technical Requirements:**
- Use the 'assemblyai' Python SDK.
- Authenticate using your `ASSEMBLYAI_API_KEY`.
- **Step 1 (Transcribe):** First, create a `Transcriber` object and submit the audio URL for transcription. This is an asynchronous process, so you must wait for the transcript to be completed.
- **Step 2 (Use LeMUR):** Once you have the completed transcript object, you can use LeMUR.
    -   Call `lemur.summarize()`.
    -   Pass the `transcript_ids` list containing the ID of your new transcript.
    -   Provide a `context` to guide the summary (e.g., "This is a quarterly earnings call for a tech company.").
    -   Set the `final_model` to 'anthropic/claude-sonnet-5' for high quality.
- **Step 3 (Output):** Print the generated summary from the LeMUR response.

**Output Format:**
A complete Python script demonstrating the two-step process of transcription followed by LeMUR summarization.
