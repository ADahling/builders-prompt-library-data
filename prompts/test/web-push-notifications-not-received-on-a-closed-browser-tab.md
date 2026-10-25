---
title: "Web Push Notifications Not Received on a Closed Browser Tab"
slug: web-push-notifications-not-received-on-a-closed-browser-tab
stage: Test
category: "Functional Bugs"
grade: A+
score: 93
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/web-push-notifications-not-received-on-a-closed-browser-tab
---
# Web Push Notifications Not Received on a Closed Browser Tab

Implement a service worker push event listener using event.waitUntil to ensure web notifications deliver even when the browser tab is closed.

Variables: project_name

## Prompt

You are a PWA developer for {{project_name}}. The application uses a Service Worker to send web push notifications to users. The notifications work correctly when the user has the application open in a browser tab. However, if the user closes the tab, they no longer receive notifications, defeating the purpose of push notifications for re-engagement.

This is because the push event listener is not correctly set up in the service worker file to operate in the background.

**Context:**
- **Technology:** Service Worker, Web Push API.
- **Problem:** Push notifications are not being handled when the app is not in the foreground.

**Instructions:**

1.  **Explain the Service Worker's Role:** Describe how a Service Worker runs as a separate background process, independent of the browser tab, and why it is the key technology for enabling background features like push notifications.
2.  **Implement the `push` Event Listener:** In your service worker file (`sw.js`), add an event listener for the `push` event. This is the entry point for handling an incoming push message from a push service (like Firebase Cloud Messaging).
3.  **Display a Notification:** Inside the `push` event listener, use the `self.registration.showNotification()` method to display a notification to the user. The data for the notification (title, body, icon) should be parsed from the push event data (`event.data.json()`). You must wrap this asynchronous operation in `event.waitUntil()` to ensure the service worker stays alive long enough to display the notification.

**Output Format:**

- **Service Worker Role Explanation:** A summary of how service workers enable background notifications.
- **`sw.js` with Push Event Listener:** The complete code for the service worker, including the `push` event listener and the call to `showNotification()`.

## Tips

The most fundamental bug fix for making web push notifications actually work as intended.
