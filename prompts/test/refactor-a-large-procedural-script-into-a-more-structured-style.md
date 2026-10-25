---
title: "Refactor a Large Procedural Script into a More Structured Style"
slug: refactor-a-large-procedural-script-into-a-more-structured-style
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactor-a-large-procedural-script-into-a-more-structured-style
---
# Refactor a Large Procedural Script into a More Structured Style

Compare object-oriented and functional refactoring plans for a procedural script, with designs, code examples, tradeoffs, and a recommendation.

Variables: language, file_path, script_functionality_description

## Prompt

I have a long, procedural script in `{{language}}` (`{{file_path}}`) that has become difficult to maintain. It consists of a series of functions that operate on global data, and the control flow is hard to follow. I want to refactor it into a more structured and maintainable style.

Your task is to propose two different refactoring strategies: one using an Object-Oriented (OO) approach and one using a Functional Programming (FP) approach.

For each approach (OO and FP), please provide:

1.  **Conceptual Design:** A high-level design for the refactored code. 
    *   For OO: What classes would you create? What would be their responsibilities and how would they interact?
    *   For FP: What would be the core pure functions? How would you manage state? How would you compose the functions to build the final logic?
2.  **Code Snippets:** Provide "before" and "after" code snippets for a key part of the script, demonstrating how it would look after being refactored using that approach.
3.  **Pros and Cons:** Discuss the pros and cons of each approach in the context of this specific script. Which approach would be more suitable and why?

Assume the script does the following: `{{script_functionality_description}}`.

Output should be a document that compares these two powerful programming paradigms as a solution to a real-world refactoring problem.

## Tips

This prompt tackles a common problem and encourages thinking about high-level code structure and design paradigms.
