---
title: "Designing a Notification API"
slug: designing-a-notification-api
stage: Build
category: "API Design"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-notification-api
---
# Designing a Notification API

Design a user notification API with endpoints for sending, filtering, and deleting alerts, plus response formats and HTTP status codes.

Variables: message, type, status

## Prompt

Create a notification API for sending alerts to users. Include endpoint designs for:
- {POST /notifications}: Sending a new notification with fields {userId}, {{message}}, and {{type}}.
- {GET /notifications}: Retrieving notifications for a user with optional filtering by {{status}}.
- {DELETE /notifications/{notificationId}}: Deleting a specific notification. 
Define the response formats and HTTP status codes for each endpoint.

## Tips

This prompt will help you structure a notification system that enhances user engagement.
