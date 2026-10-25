---
title: "Type-Safe Form with Validation"
slug: type-safe-form-with-validation
stage: Build
category: "Frontend & Styling"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/type-safe-form-with-validation
---
# Type-Safe Form with Validation

Build a complete React form with Zod validation, React Hook Form setup, accessible errors, and styled JSX for your specified form.

## Prompt

Build a type-safe form component for [describe form]:

1. SCHEMA: Define a Zod schema for the form data:
   - All fields with types, constraints, and custom error messages
   - Cross-field validation (e.g., password confirmation)
   - Conditional required fields

2. FORM: React Hook Form integration:
   - useForm with zodResolver
   - Type-safe field registration
   - Field-level error messages displayed inline
   - Form-level error summary
   - Disabled submit button until valid
   - Loading state during submission
   - Success feedback after submission

3. UX:
   - Labels on every field (not just placeholders)
   - Input hints for complex fields
   - Real-time validation (on blur, not on change)
   - Clear error state when user starts correcting
   - Tab order is logical
   - Autofocus on first field
   - Keyboard submit (Enter key)

4. ACCESSIBILITY:
   - aria-describedby linking errors to fields
   - aria-invalid on fields with errors
   - Screen reader announcements for form errors
   - Visible focus indicators

Provide complete component code with Zod schema, form hook setup, and styled JSX.

## Tips

Forms are where most apps break. This prompt ensures type safety, validation, and accessibility in one shot. Source: aipromptlibrary.app/blog/react-javascript-prompts
