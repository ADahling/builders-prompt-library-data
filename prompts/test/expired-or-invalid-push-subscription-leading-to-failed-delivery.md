---
title: "Expired or Invalid Push Subscription Leading to Failed Delivery"
slug: expired-or-invalid-push-subscription-leading-to-failed-delivery
stage: Test
category: "Functional Bugs"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/expired-or-invalid-push-subscription-leading-to-failed-delivery
---
# Expired or Invalid Push Subscription Leading to Failed Delivery

Implement a cleanup mechanism to automatically delete stale push subscriptions from your database when delivery services return 410 errors.

Variables: project_name, backend_framework

## Prompt

You are a backend engineer for {{project_name}}. The system logs are showing a growing number of `410 Gone` or `404 Not Found` errors from the push service (e.g., Google, Mozilla) when trying to send notifications. This means the push subscriptions stored in your database are expired or invalid, and you are attempting to send messages to endpoints that no longer exist.

This pollutes your logs and wastes server resources. Your task is to implement a mechanism to automatically clean up these invalid subscriptions.

**Context:**
- **Backend:** {{backend_framework}}.
- **Problem:** The database contains stale push subscriptions.

**Instructions:**

1.  **Analyze the Stale Subscription Problem:** Explain why push subscriptions can become invalid. For example, a user might clear their browser data, uninstall the browser, or explicitly revoke notification permissions.
2.  **Implement Error Handling and Cleanup:** Modify your notification sending logic. When you send a push notification and the push service responds with a specific error code indicating an invalid subscription (`410 Gone` is the most common one), you must catch this error.
3.  **Delete the Stale Subscription:** In the error handler, after identifying the `410` status code, you must immediately delete that specific push subscription record from your database. This prevents you from ever trying to send a message to that invalid endpoint again.

**Output Format:**

- **Problem Analysis:** A clear explanation of why subscriptions become stale.
- **Backend Code with Cleanup Logic:** The complete, robust code for sending a push notification, including the `try...catch` block that checks for a `410` error and deletes the corresponding subscription from the database.

## Tips

An essential part of maintaining a healthy and efficient push notification system at scale.
