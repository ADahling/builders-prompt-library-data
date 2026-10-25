---
title: "Implementing a User Feedback Collection API"
slug: implementing-a-user-feedback-collection-api
stage: Build
category: "API Design"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-a-user-feedback-collection-api
---
# Implementing a User Feedback Collection API

Design an app feedback API with submission and retrieval endpoints, required fields, error handling, and example requests and responses.

Variables: content, rating

## Prompt

Design an API for collecting user feedback regarding the application. Include endpoints for:
- {POST /feedback}: Submitting feedback with fields {userId}, {{content}}, and {{rating}}.
- {GET /feedback/{userId}}: Retrieving feedback submitted by a user.
- Discuss response formats and error handling strategies.
- Provide examples of typical requests and responses.

## Tips

This prompt will help you gather valuable insights from users.
