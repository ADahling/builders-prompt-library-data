---
title: "Clone Full Page Layout & Component Architecture"
slug: clone-full-page-layout-component-architecture
stage: Build
category: "Website Cloning"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-full-page-layout-component-architecture
---
# Clone Full Page Layout & Component Architecture

Generate a comprehensive React component architecture and boilerplate file structure to systematically clone a website's layout and design.

Variables: target_url, page_name

## Prompt

You are a React architect. Analyze the target website and produce a complete component architecture with file structure for a pixel-perfect reproduction.

Target URL: {{target_url}}
Page to clone: {{page_name}}

Produce:

1. **Component Tree**: Visual hierarchy of all components on the page, from layout wrappers down to atomic elements.

2. **File Structure**:
```
src/
├── components/
│   ├── layout/          # Header, Footer, Sidebar, Container
│   ├── sections/        # Hero, Features, Pricing, Testimonials
│   ├── ui/              # Button, Card, Badge, Input, Modal
│   └── shared/          # Logo, ThemeToggle, SocialLinks
├── hooks/               # useScrollPosition, useMediaQuery, useInView
├── lib/                 # utils, cn, constants
├── styles/              # globals.css, design tokens
└── pages/               # Route-level components
```

3. **For Each Component**:
   - Props interface (TypeScript)
   - Variants and states
   - Responsive behavior
   - Animation specifications
   - Accessibility requirements

4. **Shared Patterns**:
   - Section wrapper component (max-width, padding, background)
   - Responsive grid patterns used across sections
   - Common animation patterns (fade-in-up, stagger-children)

5. **Data Flow**:
   - Which components need external data vs static content
   - State management approach
   - API integration points

Output the complete file structure with skeleton code for every component, ready to be filled in with exact styling.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Produces the complete React component architecture for any page. The foundation for systematic cloning.
