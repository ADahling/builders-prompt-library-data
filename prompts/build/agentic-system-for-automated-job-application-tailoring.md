---
title: "Agentic System for Automated Job Application Tailoring"
slug: agentic-system-for-automated-job-application-tailoring
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-system-for-automated-job-application-tailoring
---
# Agentic System for Automated Job Application Tailoring

Get a three-agent Python pipeline that tailors a resume and cover letter to a job posting and saves them as separate text files.

Variables: resume, cover_letter, job_description

## Prompt

Design a multi-agent system that tailors a user's resume and cover letter for a specific job application.

**The Goal:**

Customize a generic `{{resume}}` and `{{cover_letter}}` for a job posting with the description `{{job_description}}`.

**The Agent Crew:**

1.  **Job Description Analyzer Agent:**
    *   **Task:** Analyze the job description and extract the top 5 most important keywords and required skills.
2.  **Resume Tailoring Agent:**
    *   **Task:** Rewrite the user's resume to highlight the experiences and skills that match the keywords extracted by the analyzer. It should not invent new experiences.
3.  **Cover Letter Writer Agent:**
    *   **Task:** Rewrite the generic cover letter to specifically address the company and the requirements mentioned in the job description. It should reference 1-2 key skills from the analyzer.

**The Orchestration:**

Write a Python script that runs this three-agent pipeline.

**Output:**

A Python script that outputs the tailored resume and cover letter as two separate text files.
