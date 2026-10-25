---
title: "Fix an Infinite Loop Caused by Incorrect Loop Termination"
slug: fix-an-infinite-loop-caused-by-incorrect-loop-termination
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-an-infinite-loop-caused-by-incorrect-loop-termination
---
# Fix an Infinite Loop Caused by Incorrect Loop Termination

Identify and resolve an infinite C# while loop by properly implementing queue dequeue logic to restore application performance.

## Prompt

You are a junior programmer. You have written a `while` loop that is supposed to process items from a queue until the queue is empty. However, the loop never terminates, even when the queue is empty, causing your application to hang. Your task is to find and fix the bug.

Context:
- The code is in C# and uses a `Queue<T>` data structure.
- The loop condition checks if the queue is not empty, but the code inside the loop that removes items from the queue is accidentally commented out.
- This means the loop condition is always true.

Provide:
1. The buggy C# code snippet that shows the infinite `while` loop.
2. An explanation of why the loop is not terminating and how this leads to 100% CPU usage.
3. The corrected code where the item is properly dequeued inside the loop, allowing the loop to eventually terminate.

## Tips

A simple but common logical error that is a good exercise for beginners.
