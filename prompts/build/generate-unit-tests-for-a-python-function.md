---
title: "Generate Unit Tests for a Python Function"
slug: generate-unit-tests-for-a-python-function
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-unit-tests-for-a-python-function
---
# Generate Unit Tests for a Python Function

Generate comprehensive Python unit tests for functions using the unittest framework to validate core logic, edge cases, and error handling.

Variables: function_code

## Prompt

You are an AI coding assistant. Generate a suite of unit tests for the following Python function using the `unittest` framework.

Function:
```python
{{function_code}}
```

Include tests for:
1. A valid, expected input.
2. An edge case (e.g., empty input, zero).
3. An invalid input that should raise an error.

## Tips

A practical prompt for automating test generation.
