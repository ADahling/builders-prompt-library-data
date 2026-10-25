---
title: "Refactor a Complex Function to Improve Readability and Maintainability"
slug: refactor-a-complex-function-to-improve-readability-and-maintainability
stage: Test
category: "Performance & Code"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactor-a-complex-function-to-improve-readability-and-maintainability
---
# Refactor a Complex Function to Improve Readability and Maintainability

Generate a structured refactoring proposal to simplify complex code through systematic decomposition, characterization testing, and cleanup.

Variables: project_name, language, code_snippet, function_purpose, function_problems

## Prompt

As a senior developer on the `{{project_name}}` project, I've identified a complex and hard-to-maintain function in our codebase. Your task is to analyze this function and propose a refactoring plan to improve its readability, maintainability, and testability.

Here is the function in question, written in `{{language}}`:

```{{language}}
{{code_snippet}}
```

**Analysis of the current function:**
*   **Purpose**: {{function_purpose}}
*   **Problems**: {{function_problems}} (e.g., It's too long, has high cyclomatic complexity, mixes concerns, uses unclear variable names, lacks comments).

**Your Task**:
Generate a detailed refactoring proposal. The proposal should be structured as a Markdown document that can be shared with the team for discussion before implementation.

1.  **Summary of Proposed Changes**: Start with a high-level summary of the refactoring strategy. What are the main goals of this refactoring? (e.g., "This refactoring aims to improve the function's readability by breaking it down into smaller, single-responsibility functions and providing clearer naming.")

2.  **Step-by-Step Refactoring Plan**:
    *   **Step 1: Introduce Characterization Tests**: Explain the importance of writing tests that capture the current behavior of the function before making any changes. This ensures the refactoring doesn't introduce regressions.
    *   **Step 2: Identify and Extract Helper Functions**: Analyze the provided code snippet and identify logical blocks that can be extracted into smaller, private helper functions. For each identified block, provide:
        *   The name of the new function.
        *   Its purpose.
        *   Its proposed signature (inputs and outputs).
    *   **Step 3: Refactor the Main Function**: Show the "after" version of the main function, which should now be much shorter and primarily orchestrate calls to the new helper functions.
    *   **Step 4: Improve Naming and Comments**: Suggest better names for variables and parameters. Add comments where the logic is still complex or non-obvious.

3.  **Refactored Code**: Provide the complete, refactored code, including the main function and all the new helper functions. The code should be well-commented and follow the project's style guide.

4.  **Benefits**: Briefly list the benefits of the proposed refactoring (e.g., easier to understand, simpler to test, less prone to bugs).

Constraint Checklist & Confidence Score:
1.  Is the refactoring plan detailed and systematic? Yes.
2.  Does the plan prioritize safety (i.e., by starting with tests)? Yes.
3.  Are the proposed new functions cohesive and single-responsibility? Yes.
4.  Is the final refactored code significantly more readable? Yes.
5.  Is the proposal well-structured and easy to understand? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the detailed refactoring proposal for the given function.

## Tips

Refactoring is a continuous process in any healthy codebase. This prompt provides a structured approach to planning and executing a complex refactoring task.
