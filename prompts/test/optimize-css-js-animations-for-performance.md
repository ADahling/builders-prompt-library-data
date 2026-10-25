---
title: "Optimize CSS/JS Animations for Performance"
slug: optimize-css-js-animations-for-performance
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 98
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-css-js-animations-for-performance
---
# Optimize CSS/JS Animations for Performance

Refactor CSS and JavaScript animations to eliminate layout thrashing and achieve a steady 60 FPS through performance-driven code audits.

Variables: animation_code_snippet, target_browser_compatibility, performance_metric_goal

## Prompt

You are a performance optimization expert. Analyze the provided CSS and JavaScript animation code for potential performance bottlenecks and suggest concrete, actionable improvements to achieve smoother animations, especially on lower-end devices and during high-load scenarios. Focus on minimizing layout thrashing, paint, and composite layers, leveraging hardware acceleration where appropriate. Consider techniques like `will-change`, `transform` and `opacity` for animations, debouncing/throttling JavaScript events, and using `requestAnimationFrame`. Provide specific code examples for proposed changes and justify each recommendation with an explanation of its performance impact.

**Current Animation Code Snippet:**
```html
{{animation_code_snippet}}
```

**Target Browser Compatibility:** `{{target_browser_compatibility}}` (e.g., 'Modern evergreen browsers (Chrome, Firefox, Edge, Safari)', 'IE11+')
**Performance Metric Goal:** `{{performance_metric_goal}}` (e.g., 'Maintain 60 FPS', 'Reduce CPU usage by 20%')

**Output Format:** Provide a structured response with the following sections:
1.  **Analysis Summary:** A brief overview of the primary performance issues identified.
2.  **Specific Recommendations:** A bulleted list of suggested changes, each with:
    *   **Issue:** What problem this recommendation addresses.
    *   **Recommendation:** The specific technique or code change.
    *   **Justification:** Explanation of why this improves performance.
    *   **Code Example (if applicable):** A revised code snippet demonstrating the change.
3.  **General Best Practices:** Any additional high-level advice relevant to animation performance.

## Tips

This prompt is designed for developers needing to fine-tune complex animations. It requires a detailed understanding of browser rendering pipelines and JavaScript execution contexts. The output should be highly technical and provide direct code modifications.
