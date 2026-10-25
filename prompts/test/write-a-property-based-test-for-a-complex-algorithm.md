---
title: "Write a Property-Based Test for a Complex Algorithm"
slug: write-a-property-based-test-for-a-complex-algorithm
stage: Test
category: "Testing & QA"
grade: C
score: 69
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-property-based-test-for-a-complex-algorithm
---
# Write a Property-Based Test for a Complex Algorithm

Generate comprehensive property-based tests for complex algorithms to uncover edge-case bugs across vast input spaces using automated data.

Variables: algorithm_purpose, property_based_testing_library

## Prompt

You are a software developer with a strong interest in testing. Your task is to write a property-based test for a complex algorithm that {{algorithm_purpose}}. The algorithm has a large input space, and it is difficult to test with traditional example-based testing.

Context:
- You will use a property-based testing library like {{property_based_testing_library}}.
- You need to define the properties of the algorithm that should hold true for all valid inputs.

Provide:
1. A set of properties that describe the behavior of the algorithm.
2. A property-based test that generates random inputs and verifies that the properties hold true.
3. An analysis of the test results and any bugs found by the test.

## Tips

An advanced prompt for developers who want to explore the power of property-based testing to find bugs in complex algorithms.
