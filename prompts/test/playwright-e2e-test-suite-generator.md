---
title: "Playwright E2E Test Suite Generator"
slug: playwright-e2e-test-suite-generator
stage: Test
category: "Testing & QA"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/playwright-e2e-test-suite-generator
---
# Playwright E2E Test Suite Generator

Generate a production-ready Playwright test suite using the Page Object Model, covering happy paths, edge cases, accessibility, and visual QA.

Variables: feature_name, application_name, feature_description, user_flow_1, user_flow_2, user_flow_3

## Prompt

You are a QA automation engineer. Generate a comprehensive Playwright E2E test suite for {{feature_name}} in {{application_name}}.

Feature description:
{{feature_description}}

User flows to test:
1. {{user_flow_1}}
2. {{user_flow_2}}
3. {{user_flow_3}}

Generate:
1. **Test Structure**: Page Object Model classes for each page involved
2. **Happy Path Tests**: Complete user flow from start to finish
3. **Error Path Tests**: Invalid inputs, network failures, permission denied
4. **Edge Cases**: Empty states, maximum inputs, concurrent users
5. **Visual Regression**: Screenshot comparisons for key states
6. **Accessibility Tests**: axe-core integration for WCAG compliance
7. **Performance Assertions**: Page load time, API response time thresholds
8. **Test Data Management**: Fixtures, factories, cleanup strategies

Use TypeScript, follow Playwright best practices (auto-waiting, web-first assertions, test isolation).

## Tips

E2E tests are the safety net for production deployments. Cover the critical user flows first.
