---
title: "Optimize CSS Animation Performance for Smoothness"
slug: optimize-css-animation-performance-for-smoothness
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-css-animation-performance-for-smoothness
---
# Optimize CSS Animation Performance for Smoothness

Get a bottleneck analysis, revised CSS, and rendering explanations for animations that stutter or drop frames.

Variables: current_animation_css, animated_element_selector, performance_issue_description

## Prompt

You have a CSS animation that is causing noticeable 'jank' or stuttering during playback, particularly on less powerful devices or when multiple animations are active. Your task is to analyze the provided CSS animation code, identify the performance bottlenecks (e.g., animating expensive properties like `width`, `height`, `left`, `top`, or `box-shadow`), and propose specific optimizations to achieve a smoother, more performant animation. Focus on leveraging hardware-accelerated properties (`transform`, `opacity`), using `will-change`, and considering alternative animation techniques if necessary. Provide revised CSS that demonstrates these optimizations, along with an explanation of why the original approach was problematic and how the new approach improves performance. Consider cross-browser compatibility for the proposed solutions.

**Current Animation CSS:**
```css
{{current_animation_css}}
```

**Element Being Animated:** {{animated_element_selector}}
**Observed Performance Issue:** {{performance_issue_description}} (e.g., 'stutters during expansion', 'causes layout reflows', 'frame drops')

**Output Format:** Begin with an analysis of the performance bottlenecks. Then, present the optimized CSS animation code. Conclude with a detailed explanation of the improvements made, referencing specific CSS properties and browser rendering mechanisms.

## Tips

This advanced prompt helps developers fine-tune CSS animations for optimal performance, reducing 'jank' and improving user experience through hardware acceleration techniques.
