---
title: "Agentic System for Automated Customer Support Response"
slug: agentic-system-for-automated-customer-support-response
stage: Build
category: "AI Agent Development"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-system-for-automated-customer-support-response
---
# Agentic System for Automated Customer Support Response

Get a Python pipeline that triages support tickets, searches a mock knowledge base, and drafts a customer email response.

Variables: ticket_subject, ticket_body

## Prompt

Design a multi-agent system that drafts a response to a customer support ticket.

**The Goal:**

Draft a response to a customer ticket with the subject `{{ticket_subject}}` and body `{{ticket_body}}`.

**The Agent Crew:**

1.  **Triage Agent:**
    *   **Task:** Analyze the ticket and categorize it as "Technical Issue", "Billing Question", or "General Inquiry".
2.  **Knowledge Base Agent:**
    *   **Task:** Based on the category, search a mock knowledge base (a simple dictionary in your script) for relevant help articles or information.
3.  **Drafting Agent:**
    *   **Task:** Take the original ticket and the information from the knowledge base and draft a polite and helpful response to the customer.

**The Orchestration:**

Write a Python script that runs this three-agent pipeline.

**Output:**

A Python script that outputs the final drafted email response as a string.
