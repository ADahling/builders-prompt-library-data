---
title: "Fix Memory Leak from Unsubscribed Data in a Cached Singleton Service"
slug: fix-memory-leak-from-unsubscribed-data-in-a-cached-singleton-service
stage: Test
category: "Functional Bugs"
grade: A+
score: 95
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-memory-leak-from-unsubscribed-data-in-a-cached-singleton-service
---
# Fix Memory Leak from Unsubscribed Data in a Cached Singleton Service

Implement a robust subscription cleanup pattern in a singleton service to resolve memory leaks and ensure proper garbage collection.

Variables: tech_stack

## Prompt

You are a senior software architect working on a large-scale {{tech_stack}} application. The application uses a singleton service (`DataService`) to fetch and cache application-wide reference data. Components can subscribe to updates for specific data keys. A memory leak has been detected: when components that subscribe to the service are unmounted, the service never cleans up the subscriptions. Over time, this leads to thousands of stale callback references being held in memory.

Your task is to fix the memory leak by implementing a proper unsubscribe mechanism.

**Context:**
- **Pattern:** Singleton service for data caching.
- **Problem:** The `subscriptions` object grows indefinitely.

**Leaky Singleton Service:**

```javascript
class DataService {
  constructor() {
    if (DataService.instance) {
      return DataService.instance;
    }
    this.cache = {};
    this.subscriptions = {}; // e.g., { 'countries': [callback1, callback2] }
    DataService.instance = this;
  }

  subscribe(key, callback) {
    if (!this.subscriptions[key]) {
      this.subscriptions[key] = [];
    }
    this.subscriptions[key].push(callback);
    // Missing unsubscribe logic!
  }

  // ... methods to fetch data and notify subscribers ...
}

// React Component Example
const MyComponent = () => {
  useEffect(() => {
    const dataService = new DataService();
    // The callback is created, but never removed
    dataService.subscribe('countries', (data) => console.log(data));
  }, []);

  return <div>...</div>;
};
```

**Instructions:**

1.  **Analyze the Memory Leak:** Explain exactly how the `DataService` and the `MyComponent` example create a memory leak. Describe how the closure created by the `subscribe` method prevents the component and the callback from being garbage collected.
2.  **Implement an Unsubscribe Method:** Modify the `DataService`. The `subscribe` method should now return an `unsubscribe` function. This function, when called, should remove the specific callback from the `subscriptions` array for that key.
3.  **Refactor the Component:** Rewrite the `MyComponent`'s `useEffect` hook to correctly handle the subscription lifecycle. It must call the returned `unsubscribe` function in the `useEffect` cleanup function to prevent the memory leak when the component unmounts.

**Output Format:**

- **Memory Leak Analysis:** A detailed explanation of the cause of the leak.
- **Corrected `DataService` with Unsubscribe:** The full, corrected code for the `DataService` class.
- **Refactored Component with Cleanup:** The updated `MyComponent` code showing the correct use of the `useEffect` cleanup function.

## Tips

A subtle but severe bug that requires a solid understanding of JavaScript memory management, closures, and component lifecycles.
