---
title: "Fix a Concurrency Bug Due to a Non-Atomic Check-Then-Act"
slug: fix-a-concurrency-bug-due-to-a-non-atomic-check-then-act
stage: Test
category: "Critical Bugs"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-concurrency-bug-due-to-a-non-atomic-check-then-act
---
# Fix a Concurrency Bug Due to a Non-Atomic Check-Then-Act

Resolve Python race conditions by implementing atomic file creation and distributed locking strategies to ensure data integrity in concurrent systems.

## Prompt

You are a backend developer building a file storage service. Your code checks if a file exists before creating it. However, in a concurrent environment, two requests can both check, see that the file doesn't exist, and then both try to create it, causing one to fail. This is a classic check-then-act race condition. Your task is to fix it.

Context:
- The code is written in Python and uses the `os.path.exists()` and `open()` functions.
- The file system operations are not atomic.
- You want to ensure that only one request can create the file.

Provide:
1. A Python code snippet that demonstrates the check-then-act race condition.
2. A solution that uses a file-system-level lock. For example, on Linux, you can use the `O_CREAT | O_EXCL` flags with `os.open()` to atomically create the file, which will fail if the file already exists.
3. A discussion of other ways to solve this, such as using a lock file or a distributed lock in a multi-server environment.

## Tips

A common concurrency problem that extends beyond just databases and memory.
