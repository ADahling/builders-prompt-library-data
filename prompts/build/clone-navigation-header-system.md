---
title: "Clone Navigation & Header System"
slug: clone-navigation-header-system
stage: Build
category: "Website Cloning"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-navigation-header-system
---
# Clone Navigation & Header System

Replicate a high-fidelity, responsive header and navigation system with complex scroll behaviors, mega-menus, and accessibility features.

Variables: target_url

## Prompt

You are a frontend engineer specializing in navigation systems. Reproduce the exact navigation and header behavior from the target website.

Target URL: {{target_url}}

Requirements:

1. **Desktop Navigation**:
   - Exact layout (logo position, nav items, CTA buttons, user menu)
   - Dropdown/mega-menu behavior with exact timing
   - Scroll behavior (sticky, transparent-to-solid, hide-on-scroll-down/show-on-scroll-up)
   - Active state indicators

2. **Mobile Navigation**:
   - Hamburger menu animation (slide, fade, morph to X)
   - Mobile menu layout (full-screen overlay, slide-from-side, bottom sheet)
   - Sub-menu expansion behavior
   - Body scroll lock when menu is open

3. **Responsive Transition**:
   - Exact breakpoint where desktop converts to mobile
   - Any intermediate tablet layout

4. **Micro-interactions**:
   - Hover effects on nav items
   - Focus states for keyboard navigation
   - Active/current page indicator
   - Dropdown open/close animations with exact easing

Build this as a React component using TypeScript, Tailwind CSS, and Framer Motion. Include:
- Full responsive behavior
- Keyboard navigation (Tab, Enter, Escape)
- ARIA attributes for accessibility
- Scroll position tracking for sticky behavior
- Mobile menu with body scroll lock

Output the complete component code with all sub-components.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Reproduces the exact navigation behavior including scroll effects, mobile menu, and micro-interactions.
