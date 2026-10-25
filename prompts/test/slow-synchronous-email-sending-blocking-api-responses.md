---
title: "Slow, Synchronous Email Sending Blocking API Responses"
slug: slow-synchronous-email-sending-blocking-api-responses
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/slow-synchronous-email-sending-blocking-api-responses
---
# Slow, Synchronous Email Sending Blocking API Responses

Refactor synchronous email logic into a background job queue to prevent slow external API calls from blocking user registration responses.

Variables: project_name, backend_framework, job_queue_library

## Prompt

You are a backend developer for {{project_name}}. When a user signs up, the API makes a call to an external SMTP service to send a welcome email. This process is slow and is performed synchronously within the user registration API endpoint. As a result, the user has to wait several seconds for the API request to complete, leading to a poor user experience.

Your task is to refactor this email sending logic to be asynchronous, so it does not block the API response.

**Context:**
- **Backend:** {{backend_framework}}.
- **Problem:** Synchronous, blocking I/O in a web request handler.

**Instructions:**

1.  **Analyze the Blocking I/O Problem:** Explain why performing slow, network-bound operations like sending an email directly within an API request handler is a bad practice. Describe how it impacts application performance and scalability.
2.  **Implement a Job Queue:** Propose a solution using a background job queue (e.g., {{job_queue_library}}). When a user registers, instead of sending the email directly, the API endpoint should simply add a "send_welcome_email" job to the queue. The API can then immediately return a response to the user.
3.  **Create a Background Worker:** Show how to create a separate worker process. This worker will listen for jobs on the queue. When it receives the "send_welcome_email" job, it will be responsible for actually connecting to the SMTP service and sending the email in the background, completely separate from the web request lifecycle.

**Output Format:**

- **Problem Analysis:** A clear explanation of the synchronous blocking issue.
- **Job Queue Implementation:** Code showing how the API endpoint adds a job to the queue.
- **Background Worker Implementation:** Code for the worker process that consumes jobs from the queue and sends the email.

## Tips

A fundamental backend architecture pattern for improving performance and reliability.
