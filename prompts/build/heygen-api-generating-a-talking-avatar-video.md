---
title: "HeyGen API: Generating a Talking Avatar Video"
slug: heygen-api-generating-a-talking-avatar-video
stage: Build
category: "LLM & AI Integration"
grade: C
score: 62
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/heygen-api-generating-a-talking-avatar-video
---
# HeyGen API: Generating a Talking Avatar Video

Generate a Python script using the HeyGen API and requests library to create a talking avatar video from a specific news brief script.

## Prompt

You are building an automated news service that creates daily video summaries. You want to use a realistic AI avatar to present the news. You will use the HeyGen API to generate a video of a talking avatar from a script.

Your task is to write a Python script that calls the HeyGen API to generate a video.

**Scenario:**
- **Avatar:** Use a publicly available HeyGen stock avatar ID (e.g., you can find one in their API documentation).
- **Voice:** Use a stock voice ID.
- **Script:** "Welcome to your daily news briefing. Today's top story is about the rapid advancements in artificial intelligence."

**Technical Requirements:**
- Use the 'requests' library.
- Authenticate using your `HEYGEN_API_KEY` in the `X-Api-Key` header.
- **Step 1 (Generate Video):** Make a POST request to the `https://api.heygen.com/v2/video/generate` endpoint.
- The JSON payload should include:
    - `video_inputs`: A list of scenes. For a simple video, this is one scene.
    - Inside the scene, specify the `avatar_id
