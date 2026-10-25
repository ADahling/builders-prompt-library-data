---
title: "Production Readiness: Usability & Reliability Hardening"
slug: production-readiness-usability-reliability-hardening
stage: Test
category: "Quality Audits"
grade: C
score: 64
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-readiness-usability-reliability-hardening
---
# Production Readiness: Usability & Reliability Hardening

Audit and harden application UX and resilience by identifying edge cases, empty states, and error handling gaps with actionable code fixes.

## Prompt

Act as a QA engineer and UX specialist reviewing my app for production readiness:

1. Error Recovery: For every user action that could fail (form submit, payment, data load), verify there is a clear error message, a retry option, and the app doesn't get stuck in a broken state.
2. Empty States: Every list, table, and dashboard should have a designed empty state (not just blank space). Check and fix.
3. Loading States: Every data fetch should show a loading indicator. No content jumping when data arrives.
4. Offline Behavior: What happens when the user loses internet mid-action? The app should handle this gracefully.
5. Input Edge Cases: Test all forms with extremely long text, special characters, emoji, empty submissions, and rapid repeated submissions. Fix any that break.
6. Navigation Dead Ends: Can the user always get back to where they came from? Are there any pages with no navigation?
7. Session Expiry: What happens when the user's session expires while they're working? Data should not be lost.
8. Browser Compatibility: Test in Chrome, Firefox, Safari, and mobile browsers. Flag and fix any breaking differences.

For each issue: screenshot description, expected behavior, and code fix.

## Tips

Based on Seroter's usability/reliability prompt. Catches the stuff that makes users lose trust in your app.
