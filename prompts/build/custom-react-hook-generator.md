---
title: "Custom React Hook Generator"
slug: custom-react-hook-generator
stage: Build
category: "Frontend & Styling"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/custom-react-hook-generator
---
# Custom React Hook Generator

Build a typed React hook for your chosen functionality, with state handling, cleanup, tests, JSDoc comments, and usage examples.

## Prompt

Generate a custom React hook for [describe functionality]:

Requirements:
1. TypeScript with strict generic types where applicable.
2. Return value is a well-typed tuple or object (not "any").
3. Handle ALL states: { data, isLoading, error, isError, isSuccess }.
4. Cleanup: properly clean up subscriptions, timers, and listeners on unmount.
5. Stale closure prevention: use useCallback and useRef correctly.
6. Dependency arrays: correct and complete (no eslint-disable for exhaustive-deps).
7. Error boundaries: errors should be catchable by React error boundaries.
8. Testing: include test cases covering happy path, error path, and cleanup.

Pattern:
```typescript
function use[Name]<T>(config: Config): {
  data: T | undefined;
  isLoading: boolean;
  error: Error | null;
  // ... other return values
} {
  // Implementation
}
```

Include JSDoc comments explaining usage, parameters, and return value. Provide usage examples.

## Tips

Custom hooks are the most powerful React pattern. Bad hooks create subtle bugs. Source: aipromptlibrary.app/blog/react-javascript-prompts
