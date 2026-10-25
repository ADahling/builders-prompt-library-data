---
title: "Google Gemini API: Basic Text Generation for Email Drafting"
slug: google-gemini-api-basic-text-generation-for-email-drafting
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 99
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/google-gemini-api-basic-text-generation-for-email-drafting
---
# Google Gemini API: Basic Text Generation for Email Drafting

Automate professional client follow-up emails by developing a Python script that integrates the Gemini 3 API for text generation.

Variables: client_name, project_name

## Prompt

As a software developer, you want to automate drafting professional emails using Google's Gemini API.

Create a Python script that uses the 'google-generativeai' library to generate a professional email. The email should be a follow-up to a client after a project kickoff meeting.

**Email Context:**
- **Client Name:** {{client_name}}
- **Project Name:** {{project_name}}
- **Key Discussion Points:** Scope of work, project timeline, and next steps (which include the client providing access to their staging server).

**Technical Requirements:**
- Use the Gemini 3 Flash model.
- The script should be configured with the Google AI API key via an environment variable ('GEMINI_API_KEY').
- The prompt must instruct the model to write a polite, professional, and concise follow-up email. It should summarize the key points discussed and clearly state the action item required from the client.
- The script should define variables for the client name and project name to make the prompt reusable.
- Print the generated email body to the console.

**Output Format:**
A single, executable Python script.
