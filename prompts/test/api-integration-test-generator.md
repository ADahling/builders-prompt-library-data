---
title: "API Integration Test Generator"
slug: api-integration-test-generator
stage: Test
category: "Testing & QA"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-test-generator
---
# API Integration Test Generator

Get component API integration tests with mock handlers, helpers, and CI/CD considerations covering loading, errors, retries, and caching.

## Prompt

Generate integration tests for this component:

COMPONENT: [NAME]
API CALLS: [LIST ENDPOINTS USED]
DATA FLOW: [DESCRIBE HOW DATA IS FETCHED/USED]

Generate tests covering:
1. Successful data fetch
2. Loading state display
3. Error handling
4. Empty state
5. Retry logic (if applicable)
6. Cache behavior

Mock strategy:
- MSW (Mock Service Worker) preferred
- Or Jest mocks for fetch/axios

Test scenarios:
1. Happy path (data loads, displays correctly)
2. Network error
3. Server error (500)
4. Timeout
5. Partial data
6. User interaction after load

Provide:
1. Test file with all scenarios
2. MSW handlers
3. Test utilities/helpers
4. CI/CD considerations

## Tips

Integration tests catch bugs unit tests miss. MSW is the gold standard for API mocking. Source: aipromptlibrary.app/blog/react-javascript-prompts
