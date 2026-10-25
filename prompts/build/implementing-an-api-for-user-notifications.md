---
title: "Implementing an API for User Notifications"
slug: implementing-an-api-for-user-notifications
stage: Build
category: "API Design"
grade: C
score: 63
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-an-api-for-user-notifications
---
# Implementing an API for User Notifications

Design an API for retrieving, sending, and deleting user notifications, with required fields, response formats, and error handling.

Variables: message, type

## Prompt

Create an API for managing user notifications. Include endpoints for:
- {GET /notifications/{userId}}: Retrieving notifications for a user.
- {POST /notifications}: Sending a new notification with fields {userId}, {{message}}, and {{type}}.
- {DELETE /notifications/{notificationId}}: Deleting a specific notification. Discuss response formats and error handling.

## Tips

This prompt will help you facilitate user engagement through notifications.
