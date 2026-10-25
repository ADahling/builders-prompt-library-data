---
title: "Optimize the Performance of a React Context"
slug: optimize-the-performance-of-a-react-context-1
stage: Test
category: "Performance & Code"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-the-performance-of-a-react-context-1
---
# Optimize the Performance of a React Context

Get guidance on splitting contexts, memoization, state colocation, selectors, and alternatives when React Context causes unnecessary re-renders.

## Prompt

We are using React Context in our application to manage global state, but we are finding that it is causing unnecessary re-renders of components that are not consuming the part of the context that has changed. I need a set of best practices for optimizing the performance of React Context.

Act as a React performance expert and provide a comprehensive guide to optimizing the performance of React Context.

Your response should cover the following:
1. **Splitting Contexts:** A guide to splitting a large context into smaller, more specific contexts to reduce the number of components that re-render when the context changes.
2. **Memoization:** How to use `React.memo` and `useMemo` to prevent components from re-rendering when their props have not changed, even if the context they are consuming has changed.
3. **Colocation of State:** An explanation of the principle of state colocation and how it can be used to avoid using context for state that is only needed by a small part of the application.
4. **Selectors:** How to use selectors to compute derived data from the context and avoid re-rendering components when the derived data has not changed.
5. **Alternative State Management Libraries:** A discussion of when it might be appropriate to use a more advanced state management library like Redux or MobX instead of React Context.
