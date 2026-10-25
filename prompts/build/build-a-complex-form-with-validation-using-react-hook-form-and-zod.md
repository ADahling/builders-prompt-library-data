---
title: "Build a Complex Form with Validation using React Hook Form and Zod"
slug: build-a-complex-form-with-validation-using-react-hook-form-and-zod
stage: Build
category: "Frontend & Styling"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-complex-form-with-validation-using-react-hook-form-and-zod
---
# Build a Complex Form with Validation using React Hook Form and Zod

Build a TypeScript registration form with React Hook Form and Zod, including nested address fields, conditional company details, and error messages.

Variables: app_name

## Prompt

For our user registration page on {{app_name}}, we need to build a robust and user-friendly form that captures user details, including nested fields and conditional logic. The form must have client-side validation using Zod.

Create a React component for a user registration form with the following fields:
-   Full Name (string, required)
-   Email (string, valid email format, required)
-   Password (string, min 8 characters, required)
-   Confirm Password (must match the password)
-   Address (nested object):
    -   Street (string, required)
    -   City (string, required)
    -   Country (string, required)
-   Account Type (select dropdown: 'Personal' or 'Business')
-   Company Name (string, required only if Account Type is 'Business')

Your implementation must:
1.  Use React Hook Form for form state management and submission.
2.  Define a Zod schema for the entire form shape to handle all validation rules, including the password match and the conditional 'Company Name' field.
3.  Use the '@hookform/resolvers/zod' package to connect Zod with React Hook Form.
4.  Display validation error messages next to each invalid field.
5.  The 'Company Name' field should only be visible when the 'Account Type' is 'Business'.
6.  On successful submission, the form data should be logged to the console.

Provide the complete, self-contained React component in a single TypeScript file. This includes the Zod schema, the form component, and all necessary imports.
