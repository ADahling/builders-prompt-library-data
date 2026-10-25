---
title: "Optimize Image Loading and Display Performance"
slug: optimize-image-loading-and-display-performance
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-image-loading-and-display-performance
---
# Optimize Image Loading and Display Performance

Implement modern image optimizations like responsive scaling, lazy loading, and next-gen formats to eliminate layout shifts and boost speed.

Variables: page_context, target_performance_metric, image_src_url, current_image_css

## Prompt

You are tasked with significantly improving the image loading and display performance on a critical page within the `{{page_context}}` section of our application. Currently, images are causing layout shifts (CLS), slow loading times, and are not optimized for different screen sizes or device pixel ratios. Your goal is to provide a comprehensive strategy and specific code examples to address these issues. This includes utilizing modern image formats (e.g., WebP, AVIF), implementing responsive image techniques (`srcset`, `sizes`), lazy loading, and ensuring proper image dimensions to prevent layout shifts. The solution should be robust, maintain cross-browser compatibility, and aim for a `{{target_performance_metric}}` improvement in page load speed and visual stability.

**Problematic Image Source:**
`<img src="{{image_src_url}}" alt="..." class="..." style="...">`

**Relevant Current CSS for Image:**
```css
{{current_image_css}}
```

**Output Format:**
Detail the proposed optimizations, categorized by technique (e.g., 'Image Formats', 'Responsive Images', 'Lazy Loading', 'Dimensions'). For each technique, provide updated HTML `<img>` tags or CSS rules as appropriate. Explain the performance benefit of each change and how it contributes to a better user experience. Ensure the solution is practical for a production environment.

## Tips

This prompt addresses a fundamental web performance issue: image optimization. It guides the user through various modern techniques, emphasizing practical implementation and performance benefits.
