---
title: "Dead Code Elimination Guide"
slug: dead-code-elimination-guide
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 83
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/dead-code-elimination-guide
---
# Dead Code Elimination Guide

Systematically identify and remove unused exports, dependencies, and unreachable code to reduce technical debt and optimize project performance.

Variables: project_name, tech_stack, build_tool, test_coverage

## Prompt

You are a code cleanup specialist. Identify and safely remove dead code from {{project_name}}.

Project details:
- Tech stack: {{tech_stack}}
- Build tool: {{build_tool}}
- Test coverage: {{test_coverage}}

Systematic approach:
1. **Unused Exports**: Use the TypeScript compiler or tools like ts-prune to find exports with no importers
2. **Unused Dependencies**: Run depcheck to find packages in package.json that aren't imported
3. **Unreachable Code**: Find code after return statements, in impossible branches
4. **Commented-Out Code**: Remove all commented-out code (it's in git history)
5. **Unused CSS**: Use PurgeCSS or similar to find unused styles
6. **Unused Files**: Find files not imported by any other file
7. **Feature Flags**: Remove code behind permanently-off feature flags
8. **Deprecated APIs**: Find and replace usage of deprecated internal APIs

For each removal:
- What to remove (file path, line numbers)
- Why it's safe to remove
- How to verify nothing breaks
- The command to run after removal (build, test)

Always remove in small, reviewable commits.

## Tips

Dead code increases cognitive load, slows builds, and confuses new team members. Remove it ruthlessly.
