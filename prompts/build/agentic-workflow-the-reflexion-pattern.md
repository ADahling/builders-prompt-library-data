---
title: "Agentic Workflow: The 'Reflexion' Pattern"
slug: agentic-workflow-the-reflexion-pattern
stage: Build
category: "AI Agent Development"
grade: C
score: 67
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-workflow-the-reflexion-pattern
---
# Agentic Workflow: The 'Reflexion' Pattern

Get a Python Reflexion example where an actor writes a palindrome function, an evaluator critiques test failures, and retries use stored feedback.

## Prompt

Implement the "Reflexion" pattern, an agentic workflow where an agent reflects on its past mistakes to improve its future performance on the same task.

**The Concept:**

1.  **Actor:** Attempts the task.
2.  **Evaluator:** Checks if the Actor succeeded. If it failed, it generates a critique (a "reflection") explaining *why* it failed.
3.  **Memory:** The reflection is stored.
4.  **Retry:** The Actor tries again, but this time its prompt includes the reflection from the previous attempt, helping it avoid the same mistake.

**Scenario:**

Writing a Python function that passes a specific unit test.

**Implementation:**

1.  **Task:** Write a function `is_palindrome(s: str) -> bool`.
2.  **Test:** A function that asserts `is_palindrome("racecar") == True` and `is_palindrome("hello") == False`.
3.  **Actor Agent:** Generates the code.
4.  **Execution Environment:** A safe way to run the generated code against the test (e.g., using `exec` in a controlled manner, capturing exceptions).
5.  **The Loop:**
    *   Actor generates code.
    *   Run the code against the test.
    *   If it passes, break the loop.
    *   If it fails, capture the error message.
    *   Pass the failed code and the error message to the Evaluator agent to generate a reflection (e.g., "The code failed because it didn't handle uppercase letters").
    *   Append the reflection to the Actor's prompt for the next iteration.

**Output:**

A Python script demonstrating this loop. The output should show the agent failing initially, generating a reflection, and then succeeding on a subsequent attempt.
