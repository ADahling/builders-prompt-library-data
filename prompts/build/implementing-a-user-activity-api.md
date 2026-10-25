---
title: "Implementing a User Activity API"
slug: implementing-a-user-activity-api
stage: Build
category: "API Design"
grade: C
score: 64
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-a-user-activity-api
---
# Implementing a User Activity API

Design an API for logging and retrieving user activities, with user, action, and timestamp fields, response formats, and error handling.

Variables: action, timestamp

## Prompt

Design an API for logging user activities. Include endpoints for:
- {POST /activity}: Logging a new activity with fields {userId}, {{action}}, and {{timestamp}}.
- {GET /activity/{userId}}: Retrieving activities for a user. Discuss response formats and error handling.

## Tips

This prompt will help you track user interactions.
