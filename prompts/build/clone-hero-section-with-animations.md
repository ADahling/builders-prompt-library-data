---
title: "Clone Hero Section with Animations"
slug: clone-hero-section-with-animations
stage: Build
category: "Website Cloning"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-hero-section-with-animations
---
# Clone Hero Section with Animations

Recreate a high-fidelity, animated hero section from any URL using React, Framer Motion, and Tailwind CSS with full responsive support.

Variables: target_url

## Prompt

You are a creative frontend developer. Reproduce the exact hero section from the target website, including all animations and visual effects.

Target URL: {{target_url}}

Reproduce:

1. **Layout**: Exact positioning of headline, subheadline, CTA buttons, and any media (image, video, illustration, 3D element).

2. **Typography Animation**: If the headline has any animation (typewriter, word rotation, gradient shift, letter-by-letter reveal), reproduce it exactly with Framer Motion.

3. **Background Effects**: Gradient meshes, particle effects, animated blobs, video backgrounds, parallax layers — reproduce with CSS/Canvas/WebGL as appropriate.

4. **CTA Buttons**: Exact styling including hover states, click animations, gradient borders, glow effects.

5. **Scroll Trigger**: If the hero has scroll-based animations (parallax, fade-out, scale), implement with Intersection Observer or scroll event listeners.

6. **Responsive Behavior**: How the hero adapts at each breakpoint. Mobile-specific layout changes.

Build as a React component with:
- Framer Motion for animations
- Tailwind CSS for styling
- Responsive design (mobile-first)
- Performance optimization (will-change, GPU acceleration)
- Reduced motion media query support

Output complete component code with inline comments explaining each animation decision.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Reproduces hero sections with complex animations, gradients, and scroll effects. Handles video backgrounds and 3D elements.
