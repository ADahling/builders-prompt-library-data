---
title: "Design an API for a Job Board"
slug: design-an-api-for-a-job-board-name-job-board
stage: Build
category: "API Design"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-job-board-name-job-board
---
# Design an API for a Job Board

Get a job board RESTful API design for posting listings, searching jobs, applying, and managing applications, with methods, URIs, and data formats.

Variables: job_board_name

## Prompt

I am building a job board called {{job_board_name}}. I need to design the API for it.

Your task is to design the core API for the job board.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the job board (e.g., companies, jobs, candidates, applications).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Companies can post and manage job listings.
    *   Candidates can search for jobs and apply for them.
    *   Companies can manage applications.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoints, including the HTTP methods, URIs, and request/response formats.
