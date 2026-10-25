---
title: "Generate Video Captions for Enhanced Accessibility"
slug: generate-video-captions-for-enhanced-accessibility
stage: Secure
category: "Accessibility (WCAG)"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-video-captions-for-enhanced-accessibility
---
# Generate Video Captions for Enhanced Accessibility

Create synchronized WebVTT or SRT captions incorporating speaker IDs and non-verbal cues to enhance video accessibility.

Variables: video_description, video_script, audio_event_timestamps

## Prompt

You are tasked with generating accurate and synchronized captions for a video to improve its accessibility for hearing-impaired viewers. Your input includes a video description, the video's script, and timestamps for key audio events. Ensure the captions are concise, clear, and accurately reflect the spoken content, including speaker identification and any relevant non-verbal sounds (e.g., [laughter], [applause]).

Inputs:
- Video Description: {{video_description}}
- Video Script: {{video_script}}
- Audio Event Timestamps: {{audio_event_timestamps}}

Instructions:
1. Review the video description and script to understand the context and content.
2. Use the provided timestamps to accurately time the captions with the audio events.
3. Ensure captions are legible and fit within standard display limits (max 2 lines of text per caption).
4. Include speaker identification when necessary.
5. Include descriptions of important non-verbal sounds or music.

Output Format:
- Provide the captions in a structured format, such as WebVTT or SRT, ensuring synchronization with the video timestamps.

Example Output:
1
00:00:01,000 --> 00:00:04,000
[John] Welcome to our presentation on sustainable energy.

2
00:00:05,000 --> 00:00:07,000
[applause]

Use this prompt when you need to create accessible video content that requires precise and detailed captioning for an intermediate-level project.

## Tips

This prompt is ideal for developers working on accessibility features for video content. It guides the creation of captions that are synchronized with the video, suitable for intermediate projects where detailed captioning is required.
