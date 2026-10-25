---
title: "Design an API for a Data-intensive Scientific Computing Application"
slug: design-an-api-for-a-data-intensive-scientific-computing-application
stage: Build
category: "API Design"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-data-intensive-scientific-computing-application
---
# Design an API for a Data-intensive Scientific Computing Application

Architect an asynchronous API that efficiently manages heavy scientific workloads through job polling patterns and pre-signed URL data transfers.

## Prompt

I am building an application for scientific computing that will process large datasets and run complex simulations. I need to design an API that can handle these data-intensive and long-running tasks.

Your task is to design the API for this application.

**Instructions:**
1.  **Asynchronous Job Processing:** Design an API for submitting, monitoring, and retrieving the results of long-running jobs. The API should be asynchronous, allowing clients to submit a job and then poll for its status.
2.  **Large Data Transfer:** Describe a strategy for efficiently transferring large datasets between the client and the server. This could involve using a cloud storage service (e.g., AWS S3) and providing pre-signed URLs to the client.

**Output Format:**
Provide the output as a Markdown document. Describe the design of your asynchronous job processing API, including the endpoints and their request/response formats. Also, describe your strategy for large data transfer.
