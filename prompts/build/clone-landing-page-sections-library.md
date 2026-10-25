---
title: "Clone Landing Page Sections Library"
slug: clone-landing-page-sections-library
stage: Build
category: "Website Cloning"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-landing-page-sections-library
---
# Clone Landing Page Sections Library

Generate a library of pixel-perfect, responsive React components with Framer Motion animations by cloning every section of a target landing page.

Variables: target_url

## Prompt

You are a conversion-focused frontend developer. Reproduce every section type from the target landing page as reusable React components.

Target URL: {{target_url}}

For each section, produce a pixel-perfect React component:

1. **Hero Section**: Headline, subheadline, CTA, background (gradient/image/video), trust badges.
2. **Social Proof Bar**: Logo carousel of client/partner logos with auto-scroll.
3. **Features Grid**: Icon + title + description cards in 2x2, 3x3, or bento grid layout.
4. **Feature Showcase**: Alternating image-left/image-right sections with text content.
5. **Testimonials**: Card carousel or grid with avatar, quote, name, title, company.
6. **Pricing**: Plan comparison cards with feature lists and CTAs.
7. **FAQ**: Accordion with smooth expand/collapse animation.
8. **CTA Banner**: Full-width call-to-action with gradient background.
9. **Stats/Numbers**: Animated counting numbers with labels.
10. **Team/About**: Team member cards with photo, name, role, social links.
11. **Blog/Resources**: Article preview cards with image, category, title, excerpt.
12. **Footer**: Multi-column links, newsletter signup, social icons, legal links.

Each component must include:
- TypeScript props interface for content customization
- Responsive design (mobile-first)
- Framer Motion scroll-triggered animations
- Dark mode support
- Accessibility (semantic HTML, ARIA)

Output as a complete component library with a Storybook-style demo page showing all sections.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Produces a complete landing page section library from any reference site. Each section is a reusable, customizable component.
