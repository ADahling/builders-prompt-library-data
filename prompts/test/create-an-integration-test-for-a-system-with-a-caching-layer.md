---
title: "Create an Integration Test for a System with a Caching Layer"
slug: create-an-integration-test-for-a-system-with-a-caching-layer
stage: Test
category: "Testing & QA"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-integration-test-for-a-system-with-a-caching-layer
---
# Create an Integration Test for a System with a Caching Layer

Verify cache hit and miss logic by generating integration tests and cleanup scripts for a specific cache provider and data source.

Variables: cache_provider

## Prompt

You are a software engineer. Your task is to create an integration test for a system that has a caching layer. The caching layer is used to improve the performance of the system by caching the results of expensive operations.

Context:
- You need to test that the caching layer works as expected and that the system behaves correctly when the cache is hit or missed.
- You will use a real cache, such as {{cache_provider}}, in your test environment.

Provide:
1. An integration test that calls the system multiple times to test the cache hit and miss scenarios.
2. A script to clear the cache before each test run.
3. Assertions to verify that the system returns the correct data from the cache or from the underlying data source.

## Tips

A prompt for engineers who are building systems with caching and need to test their integration.
