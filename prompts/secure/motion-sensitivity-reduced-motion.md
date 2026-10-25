---
title: "Motion Sensitivity & Reduced Motion"
slug: motion-sensitivity-reduced-motion
stage: Secure
category: "Accessibility (WCAG)"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/motion-sensitivity-reduced-motion
---
# Motion Sensitivity & Reduced Motion

Audit UI animations for motion sensitivity and get reduced-motion alternatives, before/after code, playback controls, and a testing checklist.

## Prompt

Audit this UI for motion sensitivity and vestibular accessibility:

1. MOTION INVENTORY:
   - List every animation, transition, and parallax effect
   - Classify each as: essential (conveys meaning), decorative (visual flair), or navigational (page transitions)

2. REDUCED MOTION IMPLEMENTATION:
   For each animation, implement a prefers-reduced-motion alternative:
   ```css
   @media (prefers-reduced-motion: reduce) {
     .animated-element {
       animation: none;
       transition: none;
     }
   }
   ```

3. AUTO-PLAYING CONTENT:
   - Ensure all auto-playing animations can be paused (WCAG 2.2.2)
   - Provide a visible "Reduce Motion" toggle in the UI
   - No content flashes more than 3 times per second (WCAG 2.3.1)

4. SAFE ALTERNATIVES:
   - Replace sliding transitions with opacity fades
   - Replace parallax with static positioning
   - Replace animated progress bars with static percentage text
   - Replace carousel auto-rotation with manual-only navigation

Provide before/after code and a testing checklist.

## Tips

1 in 3 people experience motion sensitivity. Reduced motion isn't a nice-to-have — it's a medical necessity. Source: uxmagic.ai/blog/prompting-ai-wcag-22-accessible-ui
