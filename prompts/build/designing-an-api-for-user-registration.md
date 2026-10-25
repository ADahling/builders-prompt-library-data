---
title: "Designing an API for User Registration"
slug: designing-an-api-for-user-registration
stage: Build
category: "API Design"
grade: B
score: 73
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-an-api-for-user-registration
---
# Designing an API for User Registration

Design a user registration API with signup fields and token-based confirmation endpoints, plus response formats and error handling.

Variables: username, email, password

## Prompt

Design an API for user registration with endpoints for:
- {POST /register}: Submitting registration with {{username}}, {{email}}, and {{password}}.
- {GET /register/confirm/{token}}: Confirming registration. Discuss response formats and error handling.

## Tips

This prompt will help establish a user onboarding process.
