---
title: "Handle Unhandled Exceptions Gracefully"
slug: handle-unhandled-exceptions-gracefully
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/handle-unhandled-exceptions-gracefully
---
# Handle Unhandled Exceptions Gracefully

Implement robust C# error handling and logging strategies to prevent application crashes and improve the end-user experience.

## Prompt

You are a junior developer. Your application crashes whenever an unexpected error occurs, such as a network failure or invalid user input. Your task is to implement proper error handling to prevent crashes and provide a better user experience.

Context:
- The application is a simple desktop application written in C#.
- The code that can fail is not enclosed in a `try-catch` block.
- When the app crashes, the user sees an unhelpful system error message.

Provide:
1. An explanation of why unhandled exceptions are bad for an application.
2. An example of how to use a `try-catch` block to handle a potential `IOException` when reading a file.
3. A strategy for logging the error details for developers while showing a user-friendly message to the user.

## Tips

Teaches the basics of robust error handling.
