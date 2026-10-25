---
title: "Email Content Displaying Raw HTML Tags"
slug: email-content-displaying-raw-html-tags
stage: Test
category: "Functional Bugs"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/email-content-displaying-raw-html-tags
---
# Email Content Displaying Raw HTML Tags

Resolve email rendering issues by configuring correct MIME types and implementing multipart/alternative headers for HTML and plain text.

Variables: project_name, backend_language

## Prompt

You are a developer for {{project_name}}. The application sends HTML emails, but some users are reporting that the email appears as raw HTML code in their email client, with tags like `<h1>` and `<p>` visible instead of being rendered as formatted text.

This is because the email is being sent without the correct `Content-Type` header. It is likely being sent as `text/plain` instead of `text/html`.

**Context:**
- **Problem:** HTML emails are not being rendered as HTML.

**Instructions:**

1.  **Explain MIME Types and `Content-Type`:** Describe the purpose of the `Content-Type` header in an email. Explain the difference between `text/plain` and `text/html`. Introduce the concept of multipart emails (`multipart/alternative`) which provide both a plain text and an HTML version, allowing the email client to choose the best one to display.
2.  **Fix the Email Sending Code:** Find the part of your backend code that constructs and sends the email. Locate where the email headers are set and ensure that the `Content-Type` header is set to `text/html` or, even better, `multipart/alternative`.
3.  **Provide a Multipart Email Example:** Show the full structure of a raw multipart email. It should include the main headers, the boundary separator, the `text/plain` part with its own `Content-Type` header, and the `text/html` part with its own `Content-Type` header. This demonstrates best practice for maximum compatibility.

**Output Format:**

- **MIME Type Explanation:** A clear summary of the `Content-Type` header and multipart emails.
- **Code Fix:** The specific line of code in your {{backend_language}} email library that sets the correct header.
- **Multipart Email Structure:** A raw email example showing the full multipart structure.

## Tips

A technical but common email bug. Teaches the importance of email headers and MIME types.
