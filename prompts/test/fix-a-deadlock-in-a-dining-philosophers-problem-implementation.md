---
title: "Fix a Deadlock in a Dining Philosophers Problem Implementation"
slug: fix-a-deadlock-in-a-dining-philosophers-problem-implementation
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-deadlock-in-a-dining-philosophers-problem-implementation
---
# Fix a Deadlock in a Dining Philosophers Problem Implementation

Identify and resolve circular wait deadlocks in concurrent systems by implementing and fixing the classic Dining Philosophers problem.

## Prompt

You are a computer science student. You are implementing a solution to the classic Dining Philosophers concurrency problem. In your solution, each philosopher (thread) picks up their left fork and then their right fork. You have discovered that your solution can lead to a deadlock, where all philosophers are holding their left fork and waiting for their right fork, which is held by their neighbor. Your task is to fix the deadlock.

Context:
- There are five philosophers and five forks.
- Each philosopher is a thread, and each fork is a mutex.
- The deadlock occurs if all philosophers pick up their left fork at the same time.

Provide:
1. The code (in a language like Java or C++) that implements the flawed, deadlock-prone solution.
2. A clear explanation of the circular wait condition that leads to the deadlock.
3. A corrected solution that breaks the circular wait. One common solution is to have one of the philosophers (e.g., the last one) pick up their forks in the opposite order (right then left). Another solution is to use a global lock to ensure that only one philosopher can attempt to pick up forks at a time (though this reduces concurrency).

## Tips

A classic, academic concurrency problem that is great for testing a deep understanding of deadlocks.
