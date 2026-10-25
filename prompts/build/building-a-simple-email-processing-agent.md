---
title: "Building a Simple Email Processing Agent"
slug: building-a-simple-email-processing-agent
stage: Build
category: "AI Agent Development"
grade: C
score: 63
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-email-processing-agent
---
# Building a Simple Email Processing Agent

Get a Python script that uses an LLM to classify email subjects and bodies into four labels, with examples for basic email triage.

Variables: email_subject, email_body

## Prompt

Create an AI agent that can read an email, understand its intent, and categorize it. This is a foundational step for building more complex email automation workflows.

**Agent's Goal:**

Given the subject and body of an email, the agent should categorize it into one of the following labels: "Sales Inquiry", "Support Request", "Spam", or "General".

**Implementation:**

This is a classic classification task that can be solved with a well-crafted prompt and a single LLM call.

1.  **The Prompt:**
    *   Instruct the LLM to act as an email triage system.
    *   Provide the list of possible categories.
    *   Instruct the LLM to output only the single category label and nothing else. This makes parsing easy.
    *   Include the `{{email_subject}}` and `{{email_body}}` in the prompt.
2.  **Few-Shot Examples (Optional but Recommended):**
    *   To improve accuracy, you can include a few examples in the prompt:
        *   Email: "Subject: Question about pricing..." -> Category: "Sales Inquiry"
        *   Email: "Subject: My app is not working..." -> Category: "Support Request"

**Your Task:**

Write a Python function that takes an email subject and body, constructs this prompt, calls the LLM, and returns the category.

**Output:**

A Python script containing the function and a few examples of it categorizing different emails.
