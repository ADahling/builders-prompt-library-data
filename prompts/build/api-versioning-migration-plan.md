---
title: "API Versioning Migration Plan"
slug: api-versioning-migration-plan
stage: Build
category: "API Design"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-versioning-migration-plan
---
# API Versioning Migration Plan

Plan a breaking API version migration with a weekly timeline, consumer guidance, compatibility, testing, adoption tracking, and rollback steps.

## Prompt

Create a migration plan from API v[current] to v[next]:

Breaking changes:
[list changes]

Plan:
1. Deprecation timeline: When to announce, warn, sunset?
2. Communication: Changelog format, developer email, dashboard banner?
3. Compatibility layer: Can you support both versions simultaneously? For how long?
4. SDK updates: Which client libraries need updates?
5. Migration guide: Step-by-step for consumers, with before/after examples.
6. Testing: How to let consumers test against v[next] before cutover?
7. Monitoring: Track adoption of new version, identify stragglers.
8. Rollback: What if v[next] has critical issues after launch?
9. Sunset: Hard cutoff date and what happens to v[current] requests after?

Provide a week-by-week timeline.

## Tips

Prevents the chaos of unplanned breaking changes.
