---
title: "Optimize Performance Due to Excessive Re-renders from State Updates"
slug: optimize-performance-due-to-excessive-re-renders-from-state-updates
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-performance-due-to-excessive-re-renders-from-state-updates
---
# Optimize Performance Due to Excessive Re-renders from State Updates

Refactor components to eliminate redundant re-renders by implementing granular selectors, memoization, and optimized state management.

Variables: project_name, tech_stack, state_library, Dashboard.js

## Prompt

You are a performance optimization specialist brought in to fix a sluggish UI in the {{project_name}} dashboard, which is built with {{tech_stack}} and uses {{state_library}} for state management. The main dashboard component re-renders every time any minor piece of state changes anywhere in the application, even for state that is not relevant to the dashboard. This is causing noticeable lag and a poor user experience.

Your task is to diagnose the cause of the excessive re-renders and apply optimization techniques to ensure the component only re-renders when necessary.

**Context:**
- **Framework:** {{tech_stack}}
- **State Library:** {{state_library}} (e.g., Redux with react-redux)
- **File:** '/path/to/{{Dashboard.js}}'

**Problematic Component Snippet:**

```javascript
// Using react-redux
const Dashboard = () => {
  // This selector is too broad, causing re-renders on any state change.
  const entireState = useSelector(state => state);

  const chartData = transformDataForChart(entireState.reports);

  return (
    <div>
      <h1>Dashboard</h1>
      <p>Welcome, {entireState.user.name}</p>
      <MyChart data={chartData} />
      {/* ... many other components that use parts of entireState ... */}
    </div>
  );
};
```

**Instructions:**

1.  **Identify the Performance Bottleneck:** Explain why the `useSelector(state => state)` hook is causing the `Dashboard` component to re-render unnecessarily.
2.  **Refactor with Memoized Selectors:** Rewrite the state selection logic using more granular selectors. If using Redux, demonstrate how to use the `reselect` library to create memoized selectors for `userName` and `chartData`. The goal is to ensure that `chartData` is only re-computed when `state.reports` changes, not on every state update.
3.  **Apply Component Memoization:** The `MyChart` component is a complex, expensive component to render. Show how to wrap it with `React.memo` to prevent it from re-rendering if its `data` prop has not changed.
4.  **Explain the Benefits:** Summarize how these changes (granular selectors, memoized selectors, and component memoization) work together to improve the performance of the application.

**Output Format:**

- **Bottleneck Analysis:** A clear explanation of the performance issue.
- **Refactored Code with Memoized Selectors:** The corrected code, including the creation of `reselect` selectors and their use in the `Dashboard` component.
- **Component Memoization Example:** The `MyChart` component wrapped in `React.memo`.
- **Summary of Performance Gains:** An explanation of how the optimizations improve performance.

## Tips

A crucial prompt for teaching advanced performance optimization techniques in state-heavy applications.
