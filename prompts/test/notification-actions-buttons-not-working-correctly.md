---
title: "Notification Actions (Buttons) Not Working Correctly"
slug: notification-actions-buttons-not-working-correctly
stage: Test
category: "Functional Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/notification-actions-buttons-not-working-correctly
---
# Notification Actions (Buttons) Not Working Correctly

Implement logic within a Service Worker's notificationclick event to detect and process specific action button interactions.

Variables: project_name

## Prompt

You are a PWA developer for {{project_name}}, an email client application. You want to add action buttons to the email notifications, such as "Archive" and "Reply". You have added the `actions` property to the `showNotification()` options, and the buttons appear correctly. However, clicking them does nothing.

This is because you have not added the logic in the `notificationclick` event handler to check which action button was clicked.

**Context:**
- **Technology:** Service Worker, Web Push API.
- **Problem:** Notification action buttons are unresponsive.

**Notification Creation Code in `sw.js`:**

```javascript
self.registration.showNotification("New Email", {
  body: "You have a new message from John Doe.",
  actions: [
    { action: "archive", title: "Archive" },
    { action: "reply", title: "Reply" }
  ]
});
```

**Instructions:**

1.  **Explain Notification Actions:** Describe how the `actions` property works for creating buttons on a notification.
2.  **Handle Actions in `notificationclick`:** Modify the `notificationclick` event handler. The `event` object in this handler has an `action` property that contains the ID of the action button that was clicked (e.g., `"archive"

## Tips

Makes notifications much more powerful and interactive, turning them into mini-UIs.
