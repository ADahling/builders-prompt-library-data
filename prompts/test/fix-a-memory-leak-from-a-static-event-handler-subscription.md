---
title: "Fix a Memory Leak from a Static Event Handler Subscription"
slug: fix-a-memory-leak-from-a-static-event-handler-subscription
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-memory-leak-from-a-static-event-handler-subscription
---
# Fix a Memory Leak from a Static Event Handler Subscription

Identify and resolve C# memory leaks caused by long-lived event subscriptions using manual unsubscription or weak event patterns.

## Prompt

You are a C# developer. You have a memory leak in your WPF or Windows Forms application. You have a long-lived service (e.g., a singleton) that subscribes to an event on a short-lived object (e.g., a window). Because the service holds a reference to the window via the event subscription, the window is never garbage collected, even after it is closed.

Context:
- A static or singleton `EventManager` subscribes to an event on a `CustomerView` window.
- The `EventManager` is intended to live for the entire lifetime of the application.
- The `CustomerView` window is supposed to be garbage collected after it is closed, but it is not.

Provide:
1. A C# code snippet that demonstrates this memory leak pattern.
2. An explanation of how event subscriptions can create references between objects and cause memory leaks if not managed properly.
3. A solution that involves the short-lived object (the window) unsubscribing from the event when it is closed (e.g., in the `OnClosed` event handler). An alternative is to use a weak event pattern, where the event subscription does not create a strong reference to the subscriber.

## Tips

A classic memory leak pattern in event-driven, object-oriented applications.
