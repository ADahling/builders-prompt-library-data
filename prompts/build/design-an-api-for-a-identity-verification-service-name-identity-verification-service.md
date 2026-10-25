---
title: "Design an API for an Identity Verification Service"
slug: design-an-api-for-a-identity-verification-service-name-identity-verification-service
stage: Build
category: "API Design"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-identity-verification-service-name-identity-verification-service
---
# Design an API for an Identity Verification Service

Get an identity verification API design for document and selfie submissions, with asynchronous requests and webhook notification formats.

Variables: identity_verification_service_name

## Prompt

I am building an identity verification service called {{identity_verification_service_name}}. I need to design the API for it.

Your task is to design the core API for the service.

**Instructions:**
1.  **Verification Process:** Design an API that allows users to submit their identity documents (e.g., passport, driver's license) and a selfie for verification.
2.  **Asynchronous Workflow:** The verification process is likely to be asynchronous. Design an API that allows clients to submit a verification request and then be notified of the result via a webhook.

**Output Format:**
Provide the output as a Markdown document. Describe the design of the API, including the endpoints for submitting verification requests and the webhook notification format.
