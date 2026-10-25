---
title: "Complete Website Audit & Clone Blueprint"
slug: complete-website-audit-clone-blueprint
stage: Build
category: "Website Cloning"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/complete-website-audit-clone-blueprint
---
# Complete Website Audit & Clone Blueprint

Generate a comprehensive JSON blueprint and technical specification for replicating a target website's design system, interactions, and stack.

Variables: target_url

## Prompt

You are a senior full-stack architect specializing in website reproduction. Analyze the following website and produce a comprehensive clone blueprint.

Target URL: {{target_url}}

## Phase 1: Visual Audit
1. **Layout Architecture**: Document the grid system, breakpoints, container widths, and responsive behavior at 320px, 768px, 1024px, 1440px, and 1920px.
2. **Typography System**: Extract all font families (check Google Fonts, Adobe Fonts, or custom), sizes, weights, line-heights, and letter-spacing. Document the type scale.
3. **Color System**: Extract the complete color palette — primary, secondary, accent, neutral, success, warning, error. Include exact hex/HSL values. Note dark mode variants if present.
4. **Spacing System**: Identify the spacing scale (4px, 8px, 12px, 16px, etc.) used for padding, margins, and gaps.
5. **Component Inventory**: List every unique UI component (buttons, cards, modals, forms, navigation, footers, etc.) with their variants.

## Phase 2: Interaction Audit
1. **Animations**: Document all transitions, hover effects, scroll animations, page transitions, and loading states. Note timing functions and durations.
2. **Navigation Patterns**: Document the nav structure, mobile menu behavior, breadcrumbs, and any scroll-based nav changes.
3. **Forms & Inputs**: Document all form patterns, validation behavior, error states, and submission flows.
4. **Micro-interactions**: Tooltips, dropdowns, accordions, tabs, modals — document trigger, animation, and dismiss behavior.

## Phase 3: Technical Audit
1. **Tech Stack Detection**: Identify framework (React, Next.js, Vue, etc.), CSS approach (Tailwind, CSS Modules, styled-components), state management, and build tools.
2. **Performance Baseline**: Note Core Web Vitals targets, lazy loading patterns, image optimization approach.
3. **SEO Structure**: Document meta tags, Open Graph, structured data, sitemap, and canonical URLs.
4. **Accessibility**: Note ARIA patterns, keyboard navigation, focus management, and screen reader considerations.

Output a structured JSON blueprint that can be used as the specification for reproduction.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

The master prompt — produces a complete specification document for any website clone. Start here.
