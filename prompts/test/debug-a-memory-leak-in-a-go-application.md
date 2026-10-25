---
title: "Debug a Memory Leak in a Go Application"
slug: debug-a-memory-leak-in-a-go-application
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-memory-leak-in-a-go-application
---
# Debug a Memory Leak in a Go Application

Identify and resolve Go memory leaks by using pprof to trace stuck goroutines and implementing proper termination logic with contexts.

## Prompt

You are a Go developer. A long-running Go service is slowly consuming more and more memory. You suspect a memory leak caused by goroutines that are not terminating correctly. Your task is to find and fix the leak.

Context:
- The service spawns a new goroutine for each incoming request.
- The goroutine blocks on a channel that never receives a value, so it never exits.
- This causes the goroutine’s stack and any memory it has allocated to be leaked.

Provide:
1. A guide on how to use Go’s built-in `pprof` tool to profile the memory and identify the source of the leak, specifically by looking at the number of running goroutines.
2. A code snippet that demonstrates this common goroutine leak pattern.
3. The corrected code that ensures the goroutine will always terminate, for example by using a `context` that can be canceled or a `select` statement with a timeout.

## Tips

A common and subtle memory leak pattern in Go applications.
