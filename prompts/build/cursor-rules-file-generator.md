---
title: "Cursor Rules File Generator"
slug: cursor-rules-file-generator
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cursor-rules-file-generator
---
# Cursor Rules File Generator

Generates a comprehensive .cursorrules file tailored to your tech stack and architecture to enforce consistent coding standards and patterns.

Variables: project_type, tech_stack, architecture_pattern, coding_standards, team_size

## Prompt

You are an expert at configuring AI coding assistants. Generate a comprehensive .cursorrules file for my {{project_type}} project.

Project details:
- Tech stack: {{tech_stack}}
- Architecture: {{architecture_pattern}}
- Coding standards: {{coding_standards}}
- Team size: {{team_size}}

The .cursorrules file should include:
1. **Project Context**: What the project does, its architecture, key decisions
2. **Code Style Rules**: Naming conventions, file organization, import ordering
3. **Framework Patterns**: Preferred patterns for the tech stack (e.g., React hooks over classes)
4. **Error Handling**: How errors should be handled and reported
5. **Testing Requirements**: What should be tested, testing patterns to use
6. **Security Rules**: Never expose secrets, always validate input, etc.
7. **Performance Rules**: Lazy loading, memoization, bundle size limits
8. **Documentation Rules**: JSDoc requirements, README standards
9. **Forbidden Patterns**: Anti-patterns to avoid
10. **File Templates**: Standard templates for new components, hooks, tests

## Tips

A good .cursorrules file is the difference between AI-generated spaghetti and production-grade code.
