---
title: "Text-to-Speech: Generating Audio with OpenAI TTS API"
slug: text-to-speech-generating-audio-with-openai-tts-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/text-to-speech-generating-audio-with-openai-tts-api
---
# Text-to-Speech: Generating Audio with OpenAI TTS API

Implement a Python script using the OpenAI TTS API to convert article text into high-quality MP3 audio files with automated file saving.

## Prompt

You are developing an accessibility feature for a news website that reads articles aloud to users. You need to use OpenAI's Text-to-Speech (TTS) API to convert text into natural-sounding audio.

Your task is to write a Python script that takes a paragraph of text and converts it into an MP3 audio file.

**Input Text:**
"The latest advancements in artificial intelligence are paving the way for new innovations across all industries, from healthcare to finance."

**Technical Requirements:**
- Use the 'openai' Python library.
- Use the 'tts-1' model for good quality and speed.
- Choose a suitable voice, such as 'alloy'.
- The script must make a call to the `client.audio.speech.create()` method.
- The response from the API is a stream of audio data. Your script must save this stream to a binary file named 'article_audio.mp3'.
- After successfully saving the file, the script should print a confirmation message to the console.
- Handle the OpenAI API key securely using an environment variable.

**Output Format:**
A complete, executable Python script that generates an MP3 file from the given text.
