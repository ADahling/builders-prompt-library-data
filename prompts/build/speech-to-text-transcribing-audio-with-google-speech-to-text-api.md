---
title: "Speech-to-Text: Transcribing Audio with Google Speech-to-Text API"
slug: speech-to-text-transcribing-audio-with-google-speech-to-text-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/speech-to-text-transcribing-audio-with-google-speech-to-text-api
---
# Speech-to-Text: Transcribing Audio with Google Speech-to-Text API

Implement a Python script using the Google Cloud Speech-to-Text API to transcribe local WAV audio files into accurate text commands.

## Prompt

As a developer working on a voice command interface for an application, you need a highly accurate and robust speech-to-text service that can handle various accents and noisy environments. You've chosen Google Cloud's Speech-to-Text API.

Your task is to write a Python script that transcribes a short audio file using the Google Cloud Speech-to-Text client library.

**Scenario:**
- **Audio File:** A local audio file named 'command.wav', which is a short, clear recording of a voice command (e.g., "Hey computer, open the main dashboard"). The audio should be in a lossless format like WAV.
- **Language:** English (US).

**Technical Requirements:**
- Use the 'google-cloud-speech' Python library.
- Your script must be configured to authenticate with Google Cloud, typically via an environment variable `GOOGLE_APPLICATION_CREDENTIALS` pointing to a service account JSON file.
- The script should read the content of the 'command.wav' file.
- You must create a `RecognitionConfig` object, specifying the encoding (e.g., `LINEAR16`), sample rate (e.g., 16000), and language code ('en-US').
- You must create a `RecognitionAudio` object with the audio file's content.
- Call the `speech_client.recognize()` method with the config and audio objects.
- Process the response to extract the transcript of the most likely hypothesis and print it to the console.

**Output Format:**
A complete, executable Python script. The user must have a 'command.wav' file and have their Google Cloud authentication set up.
