---
title: "Debug a Memory Leak in a C++ Application"
slug: debug-a-memory-leak-in-a-c-application
stage: Test
category: "Critical Bugs"
grade: C
score: 69
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-memory-leak-in-a-c-application
---
# Debug a Memory Leak in a C++ Application

Identify and resolve C++ memory leaks using Valgrind diagnostics and modern smart pointer implementations to ensure application stability.

## Prompt

You are a senior C++ developer. A long-running C++ application is exhibiting a slow memory leak, consuming all available memory over several days. Your task is to use debugging tools to find and fix the leak.

Context:
- The application is a high-performance computing simulation.
- The memory is allocated using `new` but is not being properly deallocated with `delete`.
- You have access to tools like Valgrind or AddressSanitizer.

Provide:
1. A guide on how to use Valgrind to detect memory leaks and pinpoint the source of the leaked memory.
2. An example of a code pattern that commonly leads to memory leaks in C++.
3. A corrected version of the code using smart pointers (e.g., `std::unique_ptr` or `std::shared_ptr`) to manage memory automatically.

## Tips

A challenging prompt that requires expertise in C++ memory management and debugging tools.
