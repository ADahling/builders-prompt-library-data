---
title: "Resolve Service Worker Caching Serving Stale Application Shell"
slug: resolve-service-worker-caching-serving-stale-application-shell
stage: Test
category: "Functional Bugs"
grade: A+
score: 95
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-service-worker-caching-serving-stale-application-shell
---
# Resolve Service Worker Caching Serving Stale Application Shell

Debug PWA lifecycle issues and implement a manual update notification strategy to prevent service workers from serving stale app shells.

Variables: project_name

## Prompt

You are a PWA (Progressive Web App) developer for {{project_name}}. You have deployed a new version of your application, but users are reporting that they are still seeing the old version of the app shell (the main HTML, CSS, and JavaScript files). The service worker is aggressively caching the old assets and not activating the new service worker with the updated cache.

Your task is to debug the service worker lifecycle and implement a strategy to ensure users get the latest version of the application seamlessly.

**Context:**
- **Technology:** Progressive Web App with a Service Worker.
- **Caching Strategy:** The service worker uses a "cache-first" strategy for the application shell assets.

**Problematic Service Worker Snippet (`sw.js`):**

```javascript
const CACHE_NAME = "app-shell-v1";
const urlsToCache = ["/", "/styles/main.css", "/script/main.js"];

self.addEventListener("install", event => {
  event.waitUntil(
    caches.open(CACHE_NAME).then(cache => cache.addAll(urlsToCache))
  );
});

self.addEventListener("fetch", event => {
  event.respondWith(
    caches.match(event.request).then(response => {
      // Always returns from cache if found
      return response || fetch(event.request);
    })
  );
});

// The logic to handle updates is missing.
```

**Instructions:**

1.  **Explain the Service Worker Lifecycle:** Describe the service worker lifecycle (installing, waiting, activating). Explain why a new service worker (with an updated `CACHE_NAME`) doesn't immediately take control and why the old one continues to serve stale content.
2.  **Implement an Update Notification:** In your main application code, add logic to listen for the `updated` event from the service worker registration. When a new service worker is available (in the `waiting` state), you should display a UI notification (e.g., a toast or banner) to the user with a button that says "Update Available".
3.  **Trigger the Update:** When the user clicks the "Update Available" button, your code should send a message to the waiting service worker telling it to skip the waiting phase and activate immediately (`self.skipWaiting()`). The client-side code should then force a page reload to get the new assets.

**Output Format:**

- **Lifecycle Explanation:** A detailed analysis of the service worker lifecycle problem.
- **Client-Side Update Notification Code:** The JavaScript code for your main application that detects a new service worker and prompts the user to update.
- **Service Worker `skipWaiting` Logic:** The necessary additions to your `sw.js` file to handle the `skipWaiting` message and take control.

## Tips

A complex but critical aspect of PWA development that directly impacts user experience.
