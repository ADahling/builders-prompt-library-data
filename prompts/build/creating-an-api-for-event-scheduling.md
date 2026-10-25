---
title: "Creating an API for Event Scheduling"
slug: creating-an-api-for-event-scheduling
stage: Build
category: "API Design"
grade: B
score: 76
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-an-api-for-event-scheduling
---
# Creating an API for Event Scheduling

Design a REST API for scheduling events, with endpoints for retrieving, filtering, creating, and cancelling scheduled events.

Variables: date, title, description, location

## Prompt

Design an API for scheduling events. Include endpoints for:
- {GET /events}: Retrieving scheduled events with optional filtering by {{date}}.
- {POST /events}: Creating a new event with fields {{title}}, {{description}}, {{date}}, and {{location}}.
- {GET /events/{eventId}}: Retrieving details for a specific event.
- {DELETE /events/{eventId}}: Deleting an event. Discuss response formats and error handling.

## Tips

This prompt will help you manage event scheduling effectively.
