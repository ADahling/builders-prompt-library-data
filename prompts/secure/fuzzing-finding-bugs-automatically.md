---
title: "Fuzzing: Finding Bugs Automatically"
slug: fuzzing-finding-bugs-automatically
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fuzzing-finding-bugs-automatically
---
# Fuzzing: Finding Bugs Automatically

Implement a libFuzzer harness for a C++ parsing function to automatically detect memory safety bugs and security vulnerabilities.

Variables: function_signature

## Prompt

You are a software engineer who wants to improve the quality and security of your C++ application. You have heard about fuzzing as a technique to find bugs automatically. Your task is to set up a simple fuzzing harness for a function in your application using a modern fuzzing engine like libFuzzer.

Context:
- The function to be fuzzed is `{{function_signature}}`.
- The function takes a string as input and parses it.

Provide:
1. A brief explanation of what fuzzing is and how it works.
2. A code example of a fuzzing harness for the given function using libFuzzer.
3. Instructions on how to compile and run the fuzzer and what to do when it finds a crash.

## Tips

A hands-on prompt for learning a powerful technique for finding bugs and vulnerabilities in software.
