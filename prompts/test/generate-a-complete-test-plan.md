---
title: "Generate a Complete Test Plan"
slug: generate-a-complete-test-plan
stage: Test
category: "Testing & QA"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-complete-test-plan
---
# Generate a Complete Test Plan

Get an app test plan with prioritized test cases for core flows, edge cases, auth, payments, mobile, performance, and security.

## Prompt

Create a test plan for my [describe app]:

1. Test Strategy: Types needed (unit, integration, e2e, manual) and tools.
2. Critical Path Tests: For each core flow (signup, login, main feature, payment): test name, preconditions, steps, expected result, priority (P0/P1/P2).
3. Edge Cases: 3-5 per feature (empty inputs, long inputs, special chars, concurrent users, network failures, expired sessions).
4. Auth Tests: Invalid credentials, expired tokens, unauthorized access, role-based, session timeout.
5. Payment Tests: Success, failure, duplicate submission, webhook delivery, subscription expiry.
6. Mobile Tests: Critical flows on mobile sizes.
7. Performance: Page load, API response, time to interactive. Thresholds.
8. Security Tests: XSS, CSRF, SQL injection, IDOR, exposed secrets.

Table: Test ID | Category | Name | Steps | Expected | Priority.

## Tips

Run before every major release.
