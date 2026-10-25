---
title: "Duplicate Notifications Sent to a User"
slug: duplicate-notifications-sent-to-a-user
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/duplicate-notifications-sent-to-a-user
---
# Duplicate Notifications Sent to a User

Implement a timestamp-based deduplication strategy to prevent duplicate push notifications across multiple devices by targeting active sessions.

Variables: project_name, backend_framework

## Prompt

You are a backend engineer for {{project_name}}, a social media application. Users are reporting that they sometimes receive the same notification (e.g., "You have a new message") multiple times. An investigation reveals that when a user logs in on multiple devices (e.g., a laptop and a phone), they get a separate push subscription object for each. The backend is storing all of these subscriptions and sending a push message to every subscription associated with the user, resulting in duplicates.

Your task is to fix the backend logic to avoid sending duplicate notifications.

**Context:**
- **Backend:** {{backend_framework}}.
- **Problem:** One user has many push subscriptions, and the backend notifies all of them for a single event.

**Instructions:**

1.  **Analyze the Duplicate Subscription Problem:** Explain why it is normal for a single user to have multiple push subscriptions and how the current naive broadcasting approach leads to duplicates.
2.  **Propose a Deduplication Strategy:** Design a strategy to prevent duplicate notifications. A common approach is to only send the notification to the user's *most recently active* subscription. This requires adding a `last_used_at` timestamp column to your `push_subscriptions` table in the database.
3.  **Implement the Strategy:**
    *   **Update Timestamp:** Modify the backend code so that every time a user's device makes an authenticated API call, the `last_used_at` timestamp for its corresponding push subscription is updated.
    *   **Targeted Notification:** Modify the notification sending logic. Instead of fetching all subscriptions for a user, it should now fetch only the one with the most recent `last_used_at` timestamp and send the push notification to that single endpoint.

**Output Format:**

- **Problem Analysis:** A clear explanation of the cause of the duplicate notifications.
- **Deduplication Strategy:** A description of the `last_used_at` timestamp approach.
- **Implementation Code:** Code snippets for both updating the timestamp on activity and for selecting the single most recent subscription when sending a notification.

## Tips

A common issue in real-world applications with multi-device users. This teaches a practical deduplication strategy.
