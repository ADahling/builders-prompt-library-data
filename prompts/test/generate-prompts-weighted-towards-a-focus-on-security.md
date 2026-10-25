---
title: "Generate prompts weighted towards a focus on security"
slug: generate-prompts-weighted-towards-a-focus-on-security
stage: Test
category: "Code Review"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-prompts-weighted-towards-a-focus-on-security
---
# Generate prompts weighted towards a focus on security

Get a numbered markdown review guide for security-focused projects, with checks for injection, encryption, data leaks, and missing MFA.

Variables: project_name, tech_stack

## Prompt

For a project where security is a crucial focus, like {{project_name}}, generate a code review guide that highlights potential security vulnerabilities in {{tech_stack}}. This should include potential injection points, weak use of encryption, improper handling of errors leading to data leaks, and lack of multi-factor authentication. Ensure each topic includes actionable points reviewers can look for. The output should be a markdown document with numbered list items.
