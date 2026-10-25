---
title: "Generate Detailed Audio Descriptions for Visual Content"
slug: generate-detailed-audio-descriptions-for-visual-content
stage: Secure
category: "Accessibility (WCAG)"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-detailed-audio-descriptions-for-visual-content
---
# Generate Detailed Audio Descriptions for Visual Content

Generate precise, objective audio descriptions to make visual media accessible and immersive for users with visual impairments.

Variables: content_title, content_type

## Prompt

You are tasked with creating comprehensive audio descriptions for a series of visual content pieces. Your goal is to enable visually impaired users to fully experience and understand the visual elements and context. Follow the instructions below to generate effective audio descriptions.

1. **Input Details**: Provide specific details about the visual content, including:
   - **Content Title**: {{content_title}}
   - **Content Type**: {{content_type}} (e.g., movie, educational video, art piece)
   - **Key Visual Elements**: List the major visual components that need description, such as colors, movements, characters, and settings.
   - **Intended Audience**: Describe who the audio description is for (e.g., children, adults, learners).

2. **Description Requirements**:
   - **Clarity and Conciseness**: Ensure descriptions are clear and to the point, avoiding unnecessary jargon.
   - **Chronological Order**: Describe events in the order they occur to maintain narrative flow.
   - **Emotional Tone**: Convey the emotional tone of the scene accurately.
   - **Objective Observation**: Focus on objective details without personal interpretation or opinion.

3. **Output Format**:
   - **Audio Description Title**: A brief title for the description.
   - **Description Text**: A paragraph that provides an immersive experience, enabling the listener to visualize the content. The description should include details about setting, actions, expressions, and any other relevant visual cues.

Example Output:
{
   "Audio Description Title": "Opening Scene of {{content_title}}",
   "Description Text": "The scene opens with a panoramic view of a bustling cityscape under a clear blue sky. Tall skyscrapers glisten in the morning sun, while cars and pedestrians fill the busy streets below. The camera slowly zooms in on a young woman standing at a bus stop, her expression a mix of anticipation and anxiety as she checks her watch."
}

Use this prompt whenever you need to create audio descriptions that enhance accessibility and provide a richer experience for visually impaired users viewing visual content.

## Tips

Use this prompt to create detailed and engaging audio descriptions for any visual content intended for visually impaired audiences. It ensures the descriptions are informative and maintain the narrative flow, enhancing the user's experience.
