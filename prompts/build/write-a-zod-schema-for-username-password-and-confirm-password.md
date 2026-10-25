---
title: "Write a Zod Schema for Username, Password, and Confirm Password"
slug: write-a-zod-schema-for-username-password-and-confirm-password
stage: Build
category: "Frontend & Styling"
grade: B
score: 72
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-zod-schema-for-username-password-and-confirm-password
---
# Write a Zod Schema for Username, Password, and Confirm Password

Get a Zod schema and data validation example for a form with username length limits, password complexity rules, and matching confirmation.

## Prompt

I'm building a form with complex validation logic. I want to use Zod to define the validation schema. The form has a field for a username, which must be a string with a minimum of 3 characters and a maximum of 20 characters. It also has a field for a password, which must be a string with a minimum of 8 characters and contain at least one uppercase letter, one lowercase letter, and one number. Finally, there's a 'confirm password' field that must match the password. Create a Zod schema for this form and show how to use it to validate a form data object.
