---
title: "AI Code Review Prompt"
slug: ai-code-review-prompt
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/ai-code-review-prompt
---
# AI Code Review Prompt

Analyze code for bugs, security flaws, and performance bottlenecks while receiving specific line-by-line fixes and a prioritized action plan.

Variables: file_name, project_type, language, code_to_review

## Prompt

You are a senior code reviewer. Review the following code for {{file_name}} in my {{project_type}} project.

```{{language}}
{{code_to_review}}
```

Review for:
1. **Correctness**: Does the code do what it's supposed to? Are there logic errors?
2. **Security**: SQL injection, XSS, auth bypass, data exposure?
3. **Performance**: N+1 queries, unnecessary re-renders, memory leaks?
4. **Readability**: Clear naming, appropriate comments, consistent style?
5. **Error Handling**: Are all error cases handled? Are errors informative?
6. **Testing**: Is this code testable? What tests are missing?
7. **Accessibility**: ARIA labels, keyboard navigation, screen reader support?

For each issue found:
- Line number(s)
- Severity: Critical / Warning / Suggestion
- The problem
- The fix (show corrected code)

End with a summary: Overall quality score (1-10) and the top 3 things to fix first.

## Tips

Use before every PR merge. Catches issues that human reviewers often miss due to familiarity bias.
