---
title: "Fix a Memory Leak in a Single-Page Application (SPA)"
slug: fix-a-memory-leak-in-a-single-page-application-spa
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-memory-leak-in-a-single-page-application-spa
---
# Fix a Memory Leak in a Single-Page Application (SPA)

Diagnose and resolve React memory leaks by identifying detached DOM nodes in Chrome DevTools and implementing proper component cleanup logic.

## Prompt

You are a frontend developer. Your React single-page application (SPA) becomes progressively slower as users navigate between different pages. You suspect a memory leak, where components are not being properly cleaned up when they are unmounted.

Context:
- The application uses a lot of event listeners and subscriptions to data streams.
- When a component is unmounted, it's not removing its event listeners or cancelling its subscriptions.
- You can use the Chrome DevTools to diagnose the issue.

Provide:
1. A guide on how to use the Chrome DevTools' memory profiler to take heap snapshots and identify detached DOM nodes, which are a sign of memory leaks.
2. An example of a React component that leaks memory by adding an event listener in `componentDidMount` (or `useEffect`) but forgetting to remove it in `componentWillUnmount` (or the `useEffect` cleanup function).
3. The corrected version of the React component that properly cleans up its resources to prevent the memory leak.

## Tips

A common problem in complex SPAs that requires good knowledge of component lifecycles.
