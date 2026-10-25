---
title: "Debug Client-Side Caching Issues"
slug: debug-client-side-caching-issues
stage: Test
category: "Functional Bugs"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-client-side-caching-issues
---
# Debug Client-Side Caching Issues

Get diagnostic and resolution steps for suspected client-side caching issues when an API fetch displays stale data instead of expected updates.

Variables: api_endpoint, old_data, expected_data

## Prompt

I suspect that client-side caching is causing stale data to be displayed in my application. When I fetch data from {{api_endpoint}}, I get {{old_data}} instead of the latest {{expected_data}}. What steps should I take to diagnose and resolve this caching issue?

## Tips

This prompt is for developers with some knowledge of caching strategies.
