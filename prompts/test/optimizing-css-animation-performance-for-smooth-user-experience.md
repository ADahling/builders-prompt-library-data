---
title: "Optimizing CSS Animation Performance for Smooth User Experience"
slug: optimizing-css-animation-performance-for-smooth-user-experience
stage: Test
category: "UX/UI Fixes"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimizing-css-animation-performance-for-smooth-user-experience
---
# Optimizing CSS Animation Performance for Smooth User Experience

Refactor sluggish CSS animations into hardware-accelerated code to achieve smooth 60 FPS performance by focusing on composite-only properties.

Variables: animation_description, browser_context, target_fps

## Prompt

You are tasked with optimizing the performance of a critical CSS animation in a web application. The animation, described as '{{animation_description}}', is currently experiencing noticeable jank and dropped frames, particularly on {{browser_context}} browsers and lower-end devices. The goal is to refactor the animation to achieve a smooth {{target_fps}} frames per second (FPS) experience without sacrificing its visual integrity. This involves leveraging best practices for hardware-accelerated animations.

Provide the current CSS keyframes and any associated styles for the animated element. Detail the observed performance issues (e.g., stuttering, delayed start, CPU/GPU spikes). Your solution should focus on transforming properties that can be efficiently hardware-accelerated, such as `transform` (for `translate`, `scale`, `rotate`) and `opacity`, instead of layout-triggering properties like `top`, `left`, `width`, `height`. Consider using the `will-change` property strategically, but with caution, to hint to the browser about upcoming transformations. Explain the performance implications of the current approach and justify each proposed change. The output should include the current CSS, a detailed analysis of the performance bottleneck, the optimized CSS with keyframes and element styles, and a clear explanation of how each change contributes to improved animation performance.

## Tips

This advanced prompt pushes developers to apply deep knowledge of browser rendering pipelines and hardware acceleration for CSS animations, crucial for high-performance UIs.
