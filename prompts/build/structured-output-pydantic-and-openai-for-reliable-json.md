---
title: "Structured Output: Pydantic and OpenAI for Reliable JSON"
slug: structured-output-pydantic-and-openai-for-reliable-json
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-pydantic-and-openai-for-reliable-json
---
# Structured Output: Pydantic and OpenAI for Reliable JSON

Generate a Python script using the instructor library and Pydantic to enforce strict data validation and schema adherence for OpenAI outputs.

## Prompt

You are building a system that requires highly reliable, validated JSON output from an LLM. Simply using JSON mode is not enough, as it doesn't guarantee the structure or data types. You will use the 'instructor' library, which leverages Pydantic to force the OpenAI model's output to conform to a specific schema.

Your task is to write a Python script that defines a Pydantic model and uses 'instructor' to get a validated JSON object from OpenAI.

**Scenario:**
- **Input Text:** "Extract user info from this text: John Doe is 30 years old and his email is john.doe@example.com. He has 2 children."
- **Pydantic Model:** You need to define a Pydantic model called `UserInfo` with the following fields:
    - `name` (string)
    - `age` (integer)
    - `email` (string, must be a valid email format)
    - `children` (integer, must be greater than or equal to 0)

**Technical Requirements:**
- Use the 'openai', 'pydantic', and 'instructor' libraries.
- Patch the OpenAI client using `instructor.patch(client=OpenAI())`.
- Define the `UserInfo` Pydantic model with appropriate type hints and validators (e.g., for email and age).
- Make the API call using the patched client. The key difference is the `response_model` parameter, which you will set to your `UserInfo` Pydantic model.
- The 'instructor' library will handle the complex prompting and validation behind the scenes.
- The script should print the resulting `UserInfo` object, which will be an instance of your Pydantic class, not just a dictionary.
- The script should also demonstrate that the data is validated. For example, you can print `type(user_info.age)` to show it's an integer.

**Output Format:**
A complete, executable Python script.
