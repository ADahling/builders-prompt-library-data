---
title: "Debug a Null Reference Dereference in C"
slug: debug-a-null-reference-dereference-in-c
stage: Test
category: "Critical Bugs"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-null-reference-dereference-in-c
---
# Debug a Null Reference Dereference in C

Identify, fix, and prevent C linked list segmentation faults by implementing null checks and defensive programming techniques.

## Prompt

You are a systems programmer. A C program you are working on is crashing with a segmentation fault. Using a debugger, you have determined the cause is a null pointer dereference. Your task is to fix the bug.

Context:
- The program manipulates a linked list, and a pointer to a node is `NULL` when it shouldn't be.
- The crash happens when trying to access a field of the `NULL` node pointer.
- The logic for handling the end of the list is flawed.

Provide:
1. A code snippet showing a typical null pointer dereference scenario in C with a linked list.
2. The corrected code that includes a check for the `NULL` pointer before dereferencing it.
3. A discussion on defensive programming techniques in C to prevent null pointer dereferences, such as using assertions.

## Tips

A core debugging skill for any C or C++ programmer.
