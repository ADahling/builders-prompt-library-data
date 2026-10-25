---
title: "Designing an API for User Feedback"
slug: designing-an-api-for-user-feedback
stage: Build
category: "API Design"
grade: C
score: 62
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-an-api-for-user-feedback
---
# Designing an API for User Feedback

Design a feedback API with submission and per-user retrieval endpoints, including content and rating fields, responses, and error handling.

Variables: content, rating

## Prompt

Create an API for collecting user feedback. Include endpoints for:
- {POST /feedback}: Submitting feedback with fields {userId}, {{content}}, and {{rating}}.
- {GET /feedback/{userId}}: Retrieving feedback submitted by a user. Discuss response formats and error handling.

## Tips

This prompt will help you gather insights from users.
