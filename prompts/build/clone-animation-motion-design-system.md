---
title: "Clone Animation & Motion Design System"
slug: clone-animation-motion-design-system
stage: Build
category: "Website Cloning"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-animation-motion-design-system
---
# Clone Animation & Motion Design System

Extract and reconstruct a website’s complete animation system into a production-ready Framer Motion library with optimized hooks and variants.

Variables: target_url

## Prompt

You are a motion design engineer. Extract and reproduce the complete animation system from the target website.

Target URL: {{target_url}}

## Animation Inventory
For every animation on the site, document:

1. **Trigger**: On load, on scroll (viewport entry), on hover, on click, on focus
2. **Property**: opacity, transform (translate, scale, rotate), color, background, border, shadow, clip-path
3. **Duration**: Exact milliseconds
4. **Easing**: cubic-bezier values or named functions (ease-in-out, spring)
5. **Delay**: Stagger delays for sequential animations
6. **Direction**: Forward, reverse, alternate

## Common Patterns to Reproduce
1. **Page Load Sequence**: Header → Hero text → Hero image → Below-fold sections (stagger timing)
2. **Scroll Reveal**: Fade-in-up for sections entering viewport (threshold, rootMargin)
3. **Hover Effects**: Button scale, card lift, image zoom, underline expand
4. **Page Transitions**: Cross-fade, slide, shared layout animations
5. **Loading States**: Skeleton shimmer, spinner, progress bar
6. **Micro-interactions**: Toggle switches, checkbox animations, input focus rings

## Implementation
Build a Framer Motion animation library:

```typescript
// animations.ts
export const fadeInUp = { ... }
export const staggerContainer = { ... }
export const scaleOnHover = { ... }
export const slideIn = { ... }
export const pageTransition = { ... }
```

Include:
- Reusable motion variants
- AnimatePresence wrapper for page transitions
- useInView hook for scroll-triggered animations
- Reduced motion support (prefers-reduced-motion)
- Performance optimization (will-change, GPU layers)

Output the complete animation library with usage examples for every pattern found on the target site.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Extracts and reproduces every animation pattern. Produces a reusable Framer Motion animation library.
