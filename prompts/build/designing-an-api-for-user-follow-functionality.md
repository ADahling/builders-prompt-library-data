---
title: "Designing an API for User Follow Functionality"
slug: designing-an-api-for-user-follow-functionality
stage: Build
category: "API Design"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-an-api-for-user-follow-functionality
---
# Designing an API for User Follow Functionality

Design a social network API for following users, listing followers, and unfollowing, with response formats and error handling.

## Prompt

Create an API for managing user follow functionality within a social network. Include endpoints for:
- {POST /follow}: Following a user with fields {followerId} and {followeeId}.
- {GET /followers/{userId}}: Retrieving a list of followers for a specific user.
- {DELETE /follow/{followId}}: Unfollowing a user. Define response formats and error handling.

## Tips

This prompt helps implement social interactions in your API.
