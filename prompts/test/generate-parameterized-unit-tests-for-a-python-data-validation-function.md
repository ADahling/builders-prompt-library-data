---
title: "Generate Parameterized Unit Tests for a Python Data Validation Function"
slug: generate-parameterized-unit-tests-for-a-python-data-validation-function
stage: Test
category: "Testing & QA"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-parameterized-unit-tests-for-a-python-data-validation-function
---
# Generate Parameterized Unit Tests for a Python Data Validation Function

Get a parameterized pytest file for a Python validator covering valid inputs, wrong types, missing fields, invalid formats, and boundary values.

Variables: function_name, function_code, file_name

## Prompt

I have a Python function, `{{function_name}}`, that validates user input data against a set of rules. I need to create a robust suite of parameterized unit tests to cover a wide range of validation scenarios.

**Instructions:**
1.  **Function to Test:**
    ```python
    {{function_code}}
    ```
2.  **Test Framework:** Use `pytest` and its `pytest.mark.parametrize` feature.
3.  **Test Scenarios:**
    *   **Valid Data:** A set of diverse, valid inputs that should pass validation.
    *   **Invalid Data Types:** Inputs with incorrect data types for each field.
    *   **Missing Fields:** Inputs with one or more required fields missing.
    *   **Invalid Formats:** Inputs with fields that do not match the required format (e.g., invalid email address, phone number).
    *   **Boundary Values:** Test with values at the boundaries of acceptable ranges (e.g., min/max length).
4.  **Output Format:** Provide a complete Python test file (`test_{{file_name}}.py`). The tests should be organized into classes or functions, with clear and descriptive names. Each parameterized test should have a meaningful ID for easy identification of failed cases.
