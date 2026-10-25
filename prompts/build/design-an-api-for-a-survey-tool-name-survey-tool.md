---
title: "Design an API for a Survey Tool"
slug: design-an-api-for-a-survey-tool-name-survey-tool
stage: Build
category: "API Design"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-survey-tool-name-survey-tool
---
# Design an API for a Survey Tool

Get a RESTful API design for a survey tool, with methods, URIs, and request/response formats for surveys, questions, responses, and results analysis.

Variables: survey_tool_name

## Prompt

I am building a survey tool called {{survey_tool_name}}, similar to SurveyMonkey or Google Forms. I need to design the API for it.

Your task is to design the core API for the survey tool.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the tool (e.g., users, surveys, questions, responses).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Creating and managing surveys.
    *   Adding questions to a survey.
    *   Collecting responses from users.
    *   Analyzing survey results.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoints, including the HTTP methods, URIs, and request/response formats.
