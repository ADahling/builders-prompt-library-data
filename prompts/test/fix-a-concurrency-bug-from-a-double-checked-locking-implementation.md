---
title: "Fix a Concurrency Bug from a Double-Checked Locking Implementation"
slug: fix-a-concurrency-bug-from-a-double-checked-locking-implementation
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-concurrency-bug-from-a-double-checked-locking-implementation
---
# Fix a Concurrency Bug from a Double-Checked Locking Implementation

Repair broken double-checked locking in Java by applying the volatile keyword to prevent memory reordering and ensure safe instantiation.

## Prompt

You are a Java developer. You have implemented a singleton using the double-checked locking pattern to be lazy-initialized in a thread-safe way. You believe it is correct, but you are told that it is broken on certain Java versions or hardware architectures due to memory reordering issues. Your task is to fix it.

Context:
- The pattern involves checking if the instance is null, then acquiring a lock, then checking again if the instance is null, and only then creating the instance.
- The problem is that a thread might see a non-null reference to the instance before the instance’s constructor has finished running. This is because the write to the instance variable and the code inside the constructor can be reordered.

Provide:
1. The classic, broken double-checked locking code in Java.
2. A detailed explanation of the memory model issues (instruction reordering) that make this pattern unsafe without proper memory barriers.
3. The corrected version of the code. The fix is to declare the instance variable as `volatile`. The `volatile` keyword ensures that the writes to the instance variable are not reordered with the code in the constructor, making the pattern thread-safe. You should also mention that the simplest and safest way to implement a singleton in modern Java is to use an enum or a static holder class.

## Tips

A famous and very subtle concurrency problem that is a rite of passage for Java experts.
