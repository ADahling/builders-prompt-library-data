---
title: "Fix an Infinite Loop in a Linked List"
slug: fix-an-infinite-loop-in-a-linked-list
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-an-infinite-loop-in-a-linked-list
---
# Fix an Infinite Loop in a Linked List

Implement Floyd’s Cycle-Finding Algorithm in C or Java to detect and resolve infinite loops caused by circular references in a linked list.

## Prompt

You are a student learning data structures. You have written code to traverse a linked list, but it is getting stuck in an infinite loop. You discover that you have accidentally created a cycle in the list, where a node’s `next` pointer points to a previous node in the list.

Context:
- The code is in C or Java.
- You have a linked list, e.g., A -> B -> C.
- You accidentally set C’s `next` pointer to point back to A, creating the cycle A -> B -> C -> A.
- Your traversal code does not detect this cycle.

Provide:
1. A code snippet that creates a cycle in a linked list.
2. The classic algorithm for detecting a cycle in a linked list: Floyd’s Cycle-Finding Algorithm, also known as the ‘tortoise and the hare’ algorithm. It uses two pointers, one that moves one step at a time (the tortoise) and one that moves two steps at a time (the hare). If there is a cycle, the hare will eventually lap the tortoise.
3. The corrected code for traversing the list that incorporates this cycle detection to prevent the infinite loop.

## Tips

A famous and elegant algorithm problem that is a great exercise for beginners.
