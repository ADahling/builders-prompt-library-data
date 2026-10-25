---
title: "Text-to-Speech: Generating Audio with ElevenLabs API"
slug: text-to-speech-generating-audio-with-elevenlabs-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/text-to-speech-generating-audio-with-elevenlabs-api
---
# Text-to-Speech: Generating Audio with ElevenLabs API

Develop a Python script using the ElevenLabs SDK to convert text into high-quality MP3 audio with secure API key management and custom voices.

## Prompt

As a developer creating an audiobook application, you require very high-quality, expressive, and natural-sounding voices. You have chosen the ElevenLabs API for its reputation in producing top-tier synthetic audio.

Your task is to write a Python script that uses the 'elevenlabs' Python SDK to convert a piece of text into an audio file.

**Input Text:**
"It was the best of times, it was the worst of times, it was the age of wisdom, it was the age of foolishness..."

**Technical Requirements:**
- Use the 'elevenlabs' Python library.
- Securely configure your ElevenLabs API key from an environment variable `ELEVENLABS_API_KEY`.
- You need to select a specific voice. First, write a small piece of code to list the available voices and their voice_ids, then choose a suitable one (e.g., a popular voice like 'Rachel' or 'Adam'). For the final script, you can hardcode the chosen voice_id.
- The script should generate the audio for the input text using the chosen voice.
- The generated audio data should be saved to a file named 'audiobook_intro.mp3'.
- Print a confirmation message upon successful file creation.

**Output Format:**
A complete Python script that demonstrates how to generate speech and save it as an MP3 file using the ElevenLabs API.
