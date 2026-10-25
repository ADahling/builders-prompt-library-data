---
title: "Create a Skeleton Loading Component with CSS Animations"
slug: create-a-skeleton-loading-component-with-css-animations
stage: Build
category: "Frontend & Styling"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-skeleton-loading-component-with-css-animations
---
# Create a Skeleton Loading Component with CSS Animations

Build a React TypeScript skeleton loader for data fetching, with configurable shapes, CSS shimmer animation, and a composed article layout.

Variables: app_name

## Prompt

To improve the perceived performance of our data-heavy application, {{app_name}}, we want to display skeleton loaders while data is being fetched. These loaders should mimic the layout of the content that is about to appear.

Create a reusable React component for a skeleton loader that can be adapted to different content shapes (e.g., avatars, text lines, cards). The loading effect should be a shimmering animation created with CSS.

The component should:
1.  Be a functional React component written in TypeScript.
2.  Accept props to control its shape and size (e.g., 'width', 'height', 'borderRadius').
3.  The shimmering animation should be a subtle gradient that moves across the skeleton shape.
4.  The animation must be created using only CSS animations and gradients. It should be performant, using 'transform' for movement.
5.  Provide a composed 'ArticleSkeleton' component that uses the basic skeleton elements to create a loader for a typical article layout (e.g., a circular avatar, a few lines of text).

Provide the complete code for the basic skeleton component, the CSS for the animation, and the composed 'ArticleSkeleton' component in a single TypeScript file.
