---
title: "Clone Mobile Responsive Behavior"
slug: clone-mobile-responsive-behavior
stage: Build
category: "Website Cloning"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-mobile-responsive-behavior
---
# Clone Mobile Responsive Behavior

Reverse-engineer a website's responsive architecture to generate a comprehensive audit and precise Tailwind CSS implementation for all screens.

Variables: target_url

## Prompt

You are a mobile-first responsive design specialist. Analyze the target website's responsive behavior and reproduce it exactly.

Target URL: {{target_url}}

Document and reproduce behavior at each breakpoint:

## Breakpoints to Test
- **320px** (iPhone SE)
- **375px** (iPhone 12/13/14)
- **428px** (iPhone 14 Pro Max)
- **768px** (iPad)
- **1024px** (iPad Pro / small laptop)
- **1280px** (laptop)
- **1440px** (desktop)
- **1920px** (large desktop)

## For Each Breakpoint, Document
1. **Layout Changes**: Column count, stack direction, visibility toggles
2. **Typography Scale**: Font size changes, line height adjustments
3. **Spacing Changes**: Padding/margin modifications
4. **Navigation**: Desktop nav → hamburger transition point and behavior
5. **Images**: Srcset/sizes, art direction changes, aspect ratio shifts
6. **Component Variants**: Cards going from horizontal to vertical, grids collapsing
7. **Touch Targets**: Minimum 44x44px tap targets on mobile
8. **Safe Areas**: Notch/dynamic island handling, bottom bar safe area

## CSS Implementation
- Tailwind responsive prefixes (sm:, md:, lg:, xl:, 2xl:)
- Container queries where appropriate
- Fluid typography (clamp())
- Aspect ratio preservation
- Scroll snap for carousels on mobile

Output a responsive audit document and the complete Tailwind CSS classes needed for every component at every breakpoint.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Ensures pixel-perfect responsive behavior across all devices. Essential for mobile-first cloning.
