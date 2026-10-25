---
title: "One-Shot Full Website Clone Prompt"
slug: one-shot-full-website-clone-prompt
stage: Build
category: "Website Cloning"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/one-shot-full-website-clone-prompt
---
# One-Shot Full Website Clone Prompt

Generate a comprehensive, production-ready React codebase that replicates any target URL's design, animations, and backend functionality.

Variables: target_url

## Prompt

You are an elite full-stack developer who specializes in rapid website reproduction. Your task is to create a pixel-perfect, fully functional clone of the following website in a single pass.

Target URL: {{target_url}}
Tech Stack: React + TypeScript + Vite + Tailwind CSS + Supabase + Framer Motion

## Instructions

1. **Analyze** the target website thoroughly — layout, colors, typography, spacing, animations, interactions, and functionality.

2. **Produce** the complete codebase:

### File Structure
```
src/
├── components/          # All UI components
├── pages/               # Route-level pages
├── hooks/               # Custom React hooks
├── lib/                 # Utilities, Supabase client, helpers
├── data/                # Static data, constants
├── styles/              # Global CSS, design tokens
└── types/               # TypeScript interfaces
```

### Requirements
- **Pixel-perfect** visual reproduction at all breakpoints
- **All animations** reproduced with Framer Motion
- **Dark mode** support with system preference detection
- **Responsive** from 320px to 1920px+
- **Accessible** (WCAG 2.1 AA) with keyboard navigation
- **SEO optimized** with React Helmet
- **Performance** optimized (lazy loading, code splitting)
- **Type-safe** with strict TypeScript (no `any`)

### For Each Page
- Complete JSX with exact layout
- All CSS via Tailwind (no inline styles except dynamic values)
- Animations with Framer Motion
- Loading and error states
- Mobile-specific adaptations

### Backend (if the site has user features)
- Supabase schema (SQL migrations)
- Row Level Security policies
- Edge Functions for server-side logic
- Auth configuration

Output the COMPLETE codebase — every file, every component, every style. Do not summarize or abbreviate. This should be copy-paste ready to run with `npm install && npm run dev`.

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

The ultimate one-shot clone prompt. Produces a complete, runnable codebase from any website URL. Use with Claude or GPT-4 for best results.
