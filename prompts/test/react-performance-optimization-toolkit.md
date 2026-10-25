---
title: "React Performance Optimization Toolkit"
slug: react-performance-optimization-toolkit
stage: Test
category: "Performance & Code"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/react-performance-optimization-toolkit
---
# React Performance Optimization Toolkit

Diagnose React bottlenecks and apply targeted optimizations like memoization, virtualization, and code splitting to boost application speed.

Variables: component_or_page, application_name, performance_issue_1, performance_issue_2

## Prompt

You are a React performance specialist. Optimize the performance of {{component_or_page}} in {{application_name}}.

Current issues:
- {{performance_issue_1}}
- {{performance_issue_2}}

Optimization toolkit:
1. **React DevTools Profiler**: How to identify the slowest components
2. **Memoization**: When to use React.memo, useMemo, useCallback (and when NOT to)
3. **Virtualization**: Implement react-window or react-virtuoso for long lists
4. **Code Splitting**: Dynamic imports for heavy components
5. **State Management**: Moving state closer to where it's used, avoiding context re-renders
6. **Suspense & Transitions**: Using startTransition for non-urgent updates
7. **Image Optimization**: Lazy loading, responsive images, blur placeholders
8. **Bundle Analysis**: Using source-map-explorer to find bloat
9. **Web Workers**: Offloading heavy computation off the main thread
10. **Benchmarking**: Before/after metrics with React Profiler API

For each optimization:
- The problem it solves
- Before code
- After code
- Expected improvement (ms saved, renders eliminated)

## Tips

Measure first, optimize second. The React Profiler is your best friend for finding actual bottlenecks.
