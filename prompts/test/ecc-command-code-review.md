---
title: "ECC Command: /code-review"
slug: ecc-command-code-review
stage: Test
category: "Code Review"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-command-code-review
---
# ECC Command: /code-review

Review uncommitted changes for security and code quality issues, with severity, line references, suggested fixes, and commit-blocking findings.

## Prompt

# Code Review

Comprehensive security and quality review of uncommitted changes:

1. Get changed files: git diff --name-only HEAD

2. For each changed file, check for:

**Security Issues (CRITICAL):**
- Hardcoded credentials, API keys, tokens
- SQL injection vulnerabilities
- XSS vulnerabilities  
- Missing input validation
- Insecure dependencies
- Path traversal risks

**Code Quality (HIGH):**
- Functions > 50 lines
- Files > 800 lines
- Nesting depth > 4 levels
- Missing error handling
- console.log statements
- TODO/FIXME comments
- Missing JSDoc for public APIs

**Best Practices (MEDIUM):**
- Mutation patterns (use immutable instead)
- Emoji usage in code/comments
- Missing tests for new code
- Accessibility issues (a11y)

3. Generate report with:
   - Severity: CRITICAL, HIGH, MEDIUM, LOW
   - File location and line numbers
   - Issue description
   - Suggested fix

4. Block commit if CRITICAL or HIGH issues found

Never approve code with security vulnerabilities!

## Tips

Source: Everything Claude Code (ECC) — Command: /code-review
