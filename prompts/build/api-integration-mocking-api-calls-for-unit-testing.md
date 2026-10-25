---
title: "API Integration: Mocking API Calls for Unit Testing"
slug: api-integration-mocking-api-calls-for-unit-testing
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-mocking-api-calls-for-unit-testing
---
# API Integration: Mocking API Calls for Unit Testing

Generate a Python unit test using unittest.mock to simulate external API responses, ensuring fast and deterministic code validation.

## Prompt

You are a software developer writing unit tests for a service that calls an external API (e.g., the OpenAI API). You cannot make real API calls in your tests as it would be slow, costly, and non-deterministic. You need to 'mock' the API call.

Your task is to write a Python script using the `unittest.mock` library to test a function that calls an API, without actually making the network request.

**Scenario:**
- **Function to Test:** A function `get_summary(text)` that internally calls `openai.ChatCompletion.create(...)` and returns the summary text.
- **Goal:** Test that `get_summary` correctly calls the OpenAI API and processes its response, without a real API call.

**Technical Requirements:**
- Use Python's built-in `unittest` framework.
- Create a test class that inherits from `unittest.TestCase`.
- Use the `@patch('openai.ChatCompletion.create')` decorator on your test method. This will replace the real OpenAI method with a mock object for the duration of the test.
- The decorator passes the mock object as an argument to the test method (e.g., `def test_summary(self, mock_create):`).
- **Configure the Mock:** Inside the test, configure the mock's return value to simulate a real API response. For example:
  `mock_create.return_value.choices[0].message.content = "This is a mock summary."`
- **Call the Function:** Call your `get_summary('some text')` function.
- **Assert:**
    -   Use `mock_create.assert_called_once()` to verify that the OpenAI API was called exactly once.
    -   Use `self.assertEqual(result, "This is a mock summary.")` to verify that your function returned the mock data.

**Output Format:**
A complete, executable Python script containing the function to be tested and the unit test class that mocks the API call.
