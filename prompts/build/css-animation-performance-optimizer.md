---
title: "CSS Animation Performance Optimizer"
slug: css-animation-performance-optimizer
stage: Build
category: "Frontend & Styling"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/css-animation-performance-optimizer
---
# CSS Animation Performance Optimizer

Refactor CSS animations to use compositor-only properties and GPU acceleration for smooth 60fps rendering and reduced layout thrashing.

Variables: component_or_page, animation_description, performance_issues

## Prompt

You are a CSS animation performance specialist. Optimize the animations in {{component_or_page}} for 60fps rendering.

Current animations:
{{animation_description}}

Performance issues:
{{performance_issues}}

Optimize:
1. **Compositor-Only Properties**: Convert animations to use only transform and opacity
2. **will-change Hints**: Where to apply (and where NOT to apply) will-change
3. **GPU Acceleration**: Force GPU compositing for heavy animations
4. **Layout Thrashing**: Identify and fix forced synchronous layouts
5. **Animation Timing**: Use requestAnimationFrame properly, avoid setTimeout
6. **Reduced Motion**: Implement prefers-reduced-motion alternatives
7. **Intersection Observer**: Only animate elements in viewport
8. **Performance Budget**: Maximum animation complexity per frame

Show before/after code and expected performance improvement for each optimization.

## Tips

Janky animations are the #1 UX complaint. 60fps means each frame must complete in 16.67ms.
