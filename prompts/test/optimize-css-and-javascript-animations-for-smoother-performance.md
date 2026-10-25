---
title: "Optimize CSS and JavaScript Animations for Smoother Performance"
slug: optimize-css-and-javascript-animations-for-smoother-performance
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-css-and-javascript-animations-for-smoother-performance
---
# Optimize CSS and JavaScript Animations for Smoother Performance

Get profiling guidance and CSS and JavaScript optimization proposals for animations with jank or low frame rates on less powerful devices.

Variables: animation_description, target_frame_rate, browser_targets, current_animation_css_js

## Prompt

The `{{animation_description}}` animation in our application is currently experiencing noticeable jank and low frame rates, particularly on less powerful devices, leading to a poor user experience. Your task is to analyze the existing animation implementation and propose a series of optimizations to achieve a smoother, high-performance animation (aiming for `{{target_frame_rate}}` frames per second). This involves leveraging hardware acceleration, minimizing layout thrashing, and strategically using CSS properties or JavaScript animation techniques. Consider using `transform` and `opacity` for CSS animations, applying `will-change`, and using `requestAnimationFrame` for JavaScript-driven animations. You should also consider performance profiling techniques to identify bottlenecks. The solution should be compatible with `{{browser_targets}}`.

**Current Animation Implementation (CSS/JavaScript snippets):**
```css
{{current_animation_css_js}}
```

**Output Format:**
1.  **Performance Bottleneck Identification:** Describe how you would profile the current animation to identify specific performance bottlenecks (e.g., layout, paint, composite). 
2.  **Proposed CSS Optimizations:** Provide updated CSS for the animation, focusing on properties that trigger hardware acceleration (`transform`, `opacity`), and the use of `will-change`. Explain the performance benefits. 
3.  **Proposed JavaScript Optimizations (if applicable):** If the animation is JavaScript-driven, suggest modifications using `requestAnimationFrame` and techniques to avoid layout thrashing. 
4.  **Comparison and Rationale:** Explain how the optimized animation differs from the original and why these changes lead to a smoother user experience and improved performance.

## Tips

This advanced prompt focuses on animation performance, requiring knowledge of browser rendering pipelines, hardware acceleration, and advanced CSS/JS animation techniques. It emphasizes practical optimization strategies.
