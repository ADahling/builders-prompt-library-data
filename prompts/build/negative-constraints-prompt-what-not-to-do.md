---
title: "Negative Constraints Prompt (What NOT to Do)"
slug: negative-constraints-prompt-what-not-to-do
stage: Build
category: "AI Coding Assistants"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/negative-constraints-prompt-what-not-to-do
---
# Negative Constraints Prompt (What NOT to Do)

Set up coding constraints for your project covering prohibited libraries, patterns, quality issues, and security risks, with named alternatives.

## Prompt

IMPORTANT: For this project, the following are PROHIBITED. Do not use, suggest, or generate any of these:

LIBRARIES & FRAMEWORKS:
- No jQuery or jQuery-like DOM manipulation
- No Moment.js (use date-fns or native Intl)
- No lodash for simple operations (use native Array/Object methods)
- No axios (use native fetch or the Supabase client)
- No CSS-in-JS (styled-components, emotion) — use Tailwind

PATTERNS:
- No class components (use functional with hooks)
- No prop drilling more than 2 levels (use context or composition)
- No barrel files (index.ts re-exports) — import directly
- No enum (use const object with 'as const')
- No 'any' type — ever. Use unknown, proper generics, or define the type.
- No useEffect for derived state (use useMemo)
- No inline styles (use Tailwind classes)

CODE QUALITY:
- No console.log in committed code (use proper logging)
- No commented-out code blocks
- No TODO comments without a linked issue
- No magic numbers (define as named constants)
- No nested ternaries deeper than one level

SECURITY:
- No API keys or secrets in client-side code
- No dangerouslySetInnerHTML without DOMPurify
- No eval() or Function() constructor
- No disabling of ESLint rules without documented reason

If you're tempted to use any of the above, tell me what you want to do and I'll suggest the correct alternative.

## Tips

Telling AI what NOT to do is often more effective than telling it what to do. Prevents the most common AI-generated code problems. Source: Research finding from prompt engineering community
