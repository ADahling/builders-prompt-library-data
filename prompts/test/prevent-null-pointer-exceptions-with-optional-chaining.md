---
title: "Prevent Null Pointer Exceptions with Optional Chaining"
slug: prevent-null-pointer-exceptions-with-optional-chaining
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/prevent-null-pointer-exceptions-with-optional-chaining
---
# Prevent Null Pointer Exceptions with Optional Chaining

Refactor JavaScript data access with optional chaining and nullish coalescing to prevent runtime crashes from missing nested API properties.

## Prompt

You are a frontend developer working with a complex JSON API response. Your JavaScript code often breaks with the error `Cannot read property 'x' of undefined` because some nested properties in the JSON are optional. Your task is to make the code more resilient.

Context:
- The code is trying to access a deeply nested property like `response.data.user.address.street`.
- Any of the intermediate properties (`data`, `user`, `address`) could be `undefined`.
- You are using a modern version of JavaScript (ES2020+).

Provide:
1. A code snippet that demonstrates the problem, crashing when an intermediate property is missing.
2. The corrected code using optional chaining (`?.`) to safely access the nested property. The expression should return `undefined` instead of crashing if any part of the chain is `null` or `undefined`.
3. An explanation of the nullish coalescing operator (`??`) and how it can be used with optional chaining to provide a default value.

## Tips

Teaches a modern and elegant way to handle null/undefined checks in JavaScript.
