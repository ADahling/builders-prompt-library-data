---
title: "OpenClaw: 'Moment Before' Daily AI Art"
slug: openclaw-moment-before-daily-ai-art
stage: Build
category: "OpenClaw"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-moment-before-daily-ai-art
---
# OpenClaw: 'Moment Before' Daily AI Art

Set up daily historical woodcut-style images showing ten seconds before an event, formatted for an e-ink screen and sent to TRMNL.

## Prompt

# "Moment Before" — Daily AI Art for E-Ink Display

## Schedule
Cron: Every day at 5:30 AM

## Pipeline
1. Fetch today's "On This Day" events from Wikipedia API
2. Pick the single most dramatic or impactful historical event
3. Generate an image in woodcut/linocut art style showing the scene TEN SECONDS BEFORE the event happened — not the event itself, but the moment right before
   - Examples: The iceberg approaching the Titanic, the apple about to fall on Newton's head, the crowd gathering before a famous speech
4. Image specs: Stark black and white, high contrast, suitable for e-ink display (800×480 resolution)
5. Push the image to TRMNL display using the TRMNL API
6. Include only the date and location as text on the image — no event description (it should be a mystery to guess)

## Style Rules
- Always woodcut/linocut style
- Always dramatic
- Always showing the moment BEFORE
- Consistent style every day

## Why It Works
The mystery element makes it a daily conversation starter. Viewers try to guess what's about to happen based on the scene.

## Tips

Daily cron automation that generates woodcut-style AI art of the moment before a historical event, for e-ink displays. From velvet-shark's gist.
