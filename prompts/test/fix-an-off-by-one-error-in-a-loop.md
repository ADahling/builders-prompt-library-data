---
title: "Fix an Off-by-One Error in a Loop"
slug: fix-an-off-by-one-error-in-a-loop
stage: Test
category: "Critical Bugs"
grade: C
score: 66
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-an-off-by-one-error-in-a-loop
---
# Fix an Off-by-One Error in a Loop

Identify, correct, and prevent off-by-one errors in Python loops through practical examples and best practices for range-based iteration.

## Prompt

You are a programmer. You have written a loop to process elements in an array, but it's either missing the last element or trying to access an element beyond the array's bounds. Your task is to identify and fix this off-by-one error.

Context:
- The code is written in Python and uses a `for` loop with a `range()` function.
- The array has 10 elements, indexed from 0 to 9.
- The loop is intended to iterate through all elements of the array.

Provide:
1. Two examples of incorrect loop conditions that would cause an off-by-one error (one that misses the last element, and one that goes out of bounds).
2. The corrected Python code for the loop that iterates through the entire array correctly.
3. A general rule to follow when using ranges or conditions in loops to avoid off-by-one errors.

## Tips

A fundamental programming bug that is important for beginners to master.
