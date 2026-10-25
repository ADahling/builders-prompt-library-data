---
title: "Generate Mock Data for Unit Tests using a Factory Library"
slug: generate-mock-data-for-unit-tests-using-a-factory-library
stage: Test
category: "Testing & QA"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-mock-data-for-unit-tests-using-a-factory-library
---
# Generate Mock Data for Unit Tests using a Factory Library

Automate the creation of realistic, customizable mock data for unit tests by generating reusable factory definitions based on TypeScript interfaces.

Variables: interface_definition, factory_library

## Prompt

I am writing unit tests for a service that depends on complex data structures. Manually creating mock data for each test is tedious and error-prone. I want to use a factory library to generate realistic and customizable mock data.

**Instructions:**
1.  **Data Model:** The data model I need to mock is defined by the following TypeScript interface:
    ```typescript
    {{interface_definition}}
    ```
2.  **Factory Library:** Use `{{factory_library}}` (e.g., Factory-Bot, Rosy, Faker.js) to create a factory for this data model.
3.  **Factory Implementation:**
    *   Define a factory that can generate a single instance of the data model with default values.
    *   The factory should allow overriding default values for specific fields.
    *   The factory should be able to generate an array of mock data objects.
4.  **Output Format:** Provide the complete code for the factory definition. Include examples of how to use the factory to generate a single object, an object with overridden properties, and an array of objects.
