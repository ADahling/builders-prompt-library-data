---
title: "Speech-to-Text: Transcribing Audio with OpenAI Whisper API"
slug: speech-to-text-transcribing-audio-with-openai-whisper-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/speech-to-text-transcribing-audio-with-openai-whisper-api
---
# Speech-to-Text: Transcribing Audio with OpenAI Whisper API

Write a Python script using the OpenAI Whisper API to transcribe local MP3 audio files into text with the whisper-1 model.

## Prompt

You are building a tool that transcribes meeting recordings into text. You need to use a reliable speech-to-text model to get accurate transcriptions.

Your task is to write a Python script that uses the OpenAI Whisper API to transcribe a local audio file.

**Scenario:**
- **Audio File:** You have an audio file named 'meeting_snippet.mp3' in the same directory as your script. (For testing, you can record a short snippet of yourself speaking).
- **Language:** The audio is in English.

**Technical Requirements:**
- Use the 'openai' Python library.
- The script must open the local audio file ('meeting_snippet.mp3') in binary read mode.
- Use the 'whisper-1' model for the transcription.
- The script should call the `client.audio.transcriptions.create()` method, passing the file object and model name.
- The API response will contain the transcribed text. Your script must extract this text and print it to the console.
- Ensure your OpenAI API key is handled securely.

**Output Format:**
A complete Python script that transcribes an audio file and prints the result. The user must provide their own 'meeting_snippet.mp3' file.
