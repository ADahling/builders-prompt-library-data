---
title: "Streaming Responses with Anthropic Claude API"
slug: streaming-responses-with-anthropic-claude-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/streaming-responses-with-anthropic-claude-api
---
# Streaming Responses with Anthropic Claude API

Implement real-time sentiment analysis by streaming Claude API responses token-by-token using the Anthropic Python SDK and sys.stdout.flush.

## Prompt

You are building a live transcription analysis tool that processes audio, sends it to a speech-to-text service, and then streams the transcribed text to the Anthropic Claude API for real-time summarization and sentiment analysis. For this task, focus on the final step: streaming a response from Claude.

Your goal is to write a Python script that demonstrates how to handle a streaming response from the Claude API using the 'anthropic' SDK.

**Scenario:**
Send a short text to Claude and stream its response. The text is: "Analyze the following customer feedback for sentiment and key issues: 'The new dashboard UI is incredibly confusing. I can't find the analytics page anymore, and the color scheme is jarring. I've been a loyal customer for five years, but this update is a major step back.'"

**Technical Requirements:**
- Use the 'anthropic' Python SDK and the 'claude-sonnet-5' model for speed.
- Make the API call using `client.messages.stream()`.
- The script must iterate through the stream and print the text from each content block delta as it arrives.
- Use `end=''` and `sys.stdout.flush()` to ensure the output appears as a continuous stream of text in the console.
- The prompt to Claude should instruct it to provide a brief, real-time analysis of the feedback.

**Output Format:**
A complete Python script that connects to the Claude API and prints the streaming response token by token.
