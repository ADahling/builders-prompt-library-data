---
title: "Speech-to-Text: Asynchronous Transcription with AssemblyAI"
slug: speech-to-text-asynchronous-transcription-with-assemblyai
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/speech-to-text-asynchronous-transcription-with-assemblyai
---
# Speech-to-Text: Asynchronous Transcription with AssemblyAI

Construct a Python script to perform asynchronous audio transcription via AssemblyAI by submitting requests, polling for status, and retrieving results.

## Prompt

You are building a podcast transcription service. Podcast audio files are often large (1+ hours), so synchronous API calls will time out. You need to use an asynchronous API like AssemblyAI.

Your task is to write a Python script that submits an audio file URL to AssemblyAI, polls for the transcription status, and retrieves the final text.

**Scenario:**
- **Audio URL:** Use a publicly accessible audio URL, e.g., `https://assembly.ai/news.mp4`.

**Technical Requirements:**
- Use the 'requests' library (or the 'assemblyai' Python SDK if preferred, but 'requests' shows the raw REST flow better).
- Authenticate using the `ASSEMBLYAI_API_KEY` environment variable in the headers.
- **Step 1 (Submit):** Make a POST request to `https://api.assemblyai.com/v2/transcript` with the `audio_url` in the JSON body. Extract the `id` from the response.
- **Step 2 (Poll):** Implement a `while` loop. Make a GET request to `https://api.assemblyai.com/v2/transcript/{id}`. Check the `status` field.
    - If `status` is 'completed', break the loop.
    - If `status` is 'error', print an error message and exit.
    - Otherwise, `time.sleep(5)` and check again.
- **Step 3 (Retrieve):** Once completed, extract the `text` field from the final response and print it.

**Output Format:**
A complete Python script demonstrating the asynchronous transcription workflow.
