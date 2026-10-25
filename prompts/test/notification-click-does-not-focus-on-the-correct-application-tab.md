---
title: "Notification Click Does Not Focus on the Correct Application Tab"
slug: notification-click-does-not-focus-on-the-correct-application-tab
stage: Test
category: "Functional Bugs"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/notification-click-does-not-focus-on-the-correct-application-tab
---
# Notification Click Does Not Focus on the Correct Application Tab

Refactor the service worker's notificationclick handler to correctly identify, focus, or open a specific chat tab using the Clients API.

Variables: project_name

## Prompt

You are a developer for {{project_name}}, a web-based chat application. When a user receives a notification and clicks on it, it should open the application and focus on the specific chat window related to the notification. However, the current implementation only opens a new, generic tab for the application's home page, or it doesn't focus the tab if it's already open.

Your task is to fix the `notificationclick` event handler in the service worker to correctly focus on the relevant window or open it to the correct URL.

**Context:**
- **Technology:** Service Worker, Web Push API.
- **Problem:** The `notificationclick` handler has incorrect window management logic.

**Instructions:**

1.  **Explain the `notificationclick` Event:** Describe the purpose of the `notificationclick` event in the service worker. Explain that this is where you define the action that occurs when a user interacts with a notification.
2.  **Implement Window Matching:** Inside the `notificationclick` handler, use `clients.matchAll()` to get a list of all open client windows (tabs) for your application. You need to loop through these clients to find one that is already open at the target URL (which should be stored in the notification's data).
3.  **Implement Focusing and Opening Logic:**
    *   **If a matching window is found:** Use `client.focus()` to bring that existing tab to the foreground.
    *   **If no matching window is found:** Use `clients.openWindow()` to open a new tab at the correct, specific URL (e.g., `/chats/123`).
    *   Remember to wrap this logic in `event.waitUntil()`.

**Output Format:**

- **Event Explanation:** A summary of the `notificationclick` event.
- **Corrected `notificationclick` Handler:** The complete, robust code for the event handler that correctly finds, focuses, or opens the appropriate application tab.

## Tips

A crucial UX feature for notifications. This makes them feel integrated and useful rather than just being simple alerts.
