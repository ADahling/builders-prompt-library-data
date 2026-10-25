---
title: "Debug Inconsistent Data Across Tabs with a Shared Web Worker Cache"
slug: debug-inconsistent-data-across-tabs-with-a-shared-web-worker-cache
stage: Test
category: "Functional Bugs"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-inconsistent-data-across-tabs-with-a-shared-web-worker-cache
---
# Debug Inconsistent Data Across Tabs with a Shared Web Worker Cache

Refactor a Shared Worker's messaging logic to correctly broadcast real-time WebSocket updates to all open browser tabs simultaneously.

Variables: project_name

## Prompt

You are a developer building a complex financial dashboard, {{project_name}}, where users can have multiple tabs open. The application uses a Shared Worker to maintain a single WebSocket connection to a real-time data feed and cache the results. However, there is a bug: when data is updated, only the most recently opened tab reflects the change. The other open tabs continue to show stale data from the worker's cache.

Your task is to fix the communication logic so that the Shared Worker broadcasts updates to all connected tabs.

**Context:**
- **Technology:** Shared Worker for cross-tab communication and caching.
- **Problem:** The worker is not broadcasting updates to all listening tabs (ports).

**Buggy Shared Worker Code (`data.worker.js`):**

```javascript
let dataCache = {};
const ports = [];

self.onconnect = (e) => {
  const port = e.ports[0];
  ports.push(port);

  // Send the initial cache to the new tab
  port.postMessage({ type: "INIT", payload: dataCache });

  port.onmessage = (msg) => {
    // Logic to handle messages from tabs
  };
};

// WebSocket connection logic
const socket = new WebSocket("wss://api.{{project_name}}.com/realtime");
socket.onmessage = (event) => {
  const newData = JSON.parse(event.data);
  dataCache[newData.id] = newData;

  // THE BUG: This only messages the last connected port
  if (ports.length > 0) {
    ports[ports.length - 1].postMessage({ type: "UPDATE", payload: newData });
  }
};
```

**Instructions:**

1.  **Identify the Broadcasting Flaw:** Pinpoint the bug in the WebSocket's `onmessage` handler and explain why it fails to update all connected tabs.
2.  **Implement a Broadcast Function:** Create a `broadcast` function within the Shared Worker. This function should iterate over the `ports` array and post the update message to every connected port.
3.  **Refactor the Worker:** Rewrite the Shared Worker code to use your new `broadcast` function, ensuring that any data update is sent to all tabs. Also, make sure to handle closed or disconnected ports by removing them from the `ports` array.

**Output Format:**

- **Flaw Analysis:** A clear explanation of the bug in the worker's communication logic.
- **Corrected Shared Worker Code:** The complete, fixed code for `data.worker.js

## Tips

A sophisticated use case involving Shared Workers, WebSockets, and multi-tab state synchronization.
