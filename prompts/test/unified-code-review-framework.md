---
title: "Unified Code Review Framework"
slug: unified-code-review-framework
stage: Test
category: "Code Review"
grade: A+
score: 95
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/unified-code-review-framework
---
# Unified Code Review Framework

Unified Code Review Framework Review this code change from multiple expert perspectives using a structured, prioritized checklist.

## Prompt

# Unified Code Review Framework

Review this code change from multiple expert perspectives using a structured, prioritized checklist.

## Input
- [paste the diff, PR, or code]
- Tech stack: [React/Node.js/TypeScript/etc.]
- Runtime: [Node version / browser targets]
- Known constraints: [e.g., cannot introduce new dependencies]

---

## Perspective 1 — Security Specialist (Priority 1)

Evaluate (✅ pass / ⚠️ concern / ❌ issue):
- SQL injection, XSS, CSRF, prototype pollution risks
- OWASP Top 10 concerns relevant to the stack
- Hardcoded secrets or credentials in code
- Authentication bypass vectors
- Authorization gaps (missing RLS, role checks)
- Input validation and sanitization
- Dependency vulnerabilities

## Perspective 2 — Architecture & Correctness (Priority 2)

- Does it do what the PR description claims?
- Edge cases handled? (null, empty, boundary values)
- Error handling: Are failures caught and handled gracefully?
- SOLID principle violations
- Tight coupling between modules
- Data migration risks
- Scalability concerns

## Perspective 3 — Performance Engineer (Priority 3)

- N+1 queries or unnecessary database calls
- Unnecessary re-renders (React) or memory leaks
- Large payloads or unbounded lists
- Missing indexes for new queries
- Inefficient data structures or algorithms
- Opportunities for memoization or caching

## Perspective 4 — Maintainability Expert (Priority 4)

- Clear naming (variables, functions, files)
- Single responsibility — does each function do one thing?
- Magic numbers or strings that should be constants
- Dead code or commented-out code
- Code repetition (DRY violations)
- Over-complex logic (cyclomatic complexity)
- Type safety gaps
- How easy is this to test and extend?

## Perspective 5 — Testing (Priority 5)

- Are tests updated for the changes?
- Do tests verify behavior, not implementation?
- Missing negative test cases or edge cases
- Missing boundary condition tests
- Integration test coverage
- Would a test failure clearly indicate what broke?

---

## Output Format

For each finding:
```
**[SEVERITY: Critical/High/Medium/Low]** — [FILE:LINE]
Perspective: [Security/Architecture/Performance/Maintainability/Testing]
Problem: [What's wrong]
Risk: [What could happen]
Fix: [Exact code suggestion]
```

## Severity Guide
- **Critical:** Security vulnerability, data loss risk → Block merge
- **High:** Bug in business logic, missing error handling → Block merge
- **Medium:** Code quality, performance, missing tests → Request changes
- **Low:** Style, naming, documentation → Comment only

Generate 3-7 ready-to-paste review comments per PR, prioritized by severity.

## Tips

Unified code review framework combining security-first agent review, multi-persona analysis, and structured checklist. Merged from three code review prompts.
