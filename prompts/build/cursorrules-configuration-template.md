---
title: ".cursorrules Configuration Template"
slug: cursorrules-configuration-template
stage: Build
category: "AI Coding Assistants"
grade: A
score: 86
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/cursorrules-configuration-template
---
# .cursorrules Configuration Template

Write a .cursorrules file for a Cursor project with standards for TypeScript, React architecture, Tailwind styling, security, and package approvals.

## Prompt

Create a .cursorrules file for my project to enforce coding standards in Cursor IDE:

```
# Project: [Your Project Name]
# Stack: [e.g., React 18, TypeScript, Tailwind CSS, Supabase]

## Code Style
- Use TypeScript strict mode. No 'any' types.
- Use functional components with hooks. No class components.
- Use named exports, not default exports (except pages).
- File naming: kebab-case for files, PascalCase for components.
- Maximum file length: 200 lines. Split if longer.

## Architecture
- Components in src/components/[feature]/
- Hooks in src/hooks/
- Types in src/types/
- Utils in src/lib/
- All API calls go through hooks, never directly in components.
- State management: React Query for server state, useState/useReducer for local state.

## Styling
- Tailwind CSS only. No inline styles. No CSS modules.
- Colors MUST use CSS variables (never hardcoded hex).
- Use shadcn/ui components. Don't reinvent existing components.
- Responsive: mobile-first. Test at 375px, 768px, 1440px.

## Security
- Never expose API keys in client code.
- All database operations through Supabase client with RLS.
- Validate all user input server-side.
- Use parameterized queries. Never string concatenation for SQL.

## What NOT to Do
- Don't add comments that just restate the code.
- Don't use deprecated React patterns (componentDidMount, etc.).
- Don't install new packages without asking first.
- Don't use lodash for simple operations that native JS handles.
- Don't use 'as any' to silence TypeScript errors.
```

Customize this template for my specific project: [describe your project, team, and conventions].

## Tips

The .cursorrules file is the most powerful Cursor feature most people don't use. It's your project's coding constitution. Source: cursor.com/docs/rules
