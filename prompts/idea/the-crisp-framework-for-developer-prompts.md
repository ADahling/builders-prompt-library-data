---
title: "The CRISP Framework for Developer Prompts"
slug: the-crisp-framework-for-developer-prompts
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/the-crisp-framework-for-developer-prompts
---
# The CRISP Framework for Developer Prompts

Draft coding requests using a framework for context, role, instructions, specifications, and output expectations when assigning AI development tasks.

## Prompt

Use this framework for any coding prompt:

C - CONTEXT: State the tech stack, framework, language, and project structure.
Example: "React 18, Next.js 14 App Router, Tailwind CSS, Supabase backend, TypeScript."

R - ROLE: Tell the AI what kind of developer to be.
Example: "Act as a senior full-stack engineer who prioritizes security and clean architecture."

I - INSTRUCTIONS: Be specific about what to build, fix, or change.
Example: "Create a user settings page with profile editing, password change, and notification preferences."

S - SPECIFICATIONS: Define constraints, patterns, and standards.
Example: "Use shadcn/ui components. All colors via CSS variables. Server-side validation on every input. Handle loading, error, and empty states."

P - POLISH: Define output format and quality bar.
Example: "Provide complete, production-ready code. Include TypeScript types. Add inline comments for complex logic. No placeholder data."

Template:
[CONTEXT]: I'm building [app] with [stack].
[ROLE]: Act as [type of developer].
[INSTRUCTIONS]: [What to do].
[SPECIFICATIONS]: [Constraints and standards].
[POLISH]: [Output format and quality expectations].

## Tips

From DEV Community prompt engineering guides. Works in any AI tool. The structure alone improves output quality dramatically.
