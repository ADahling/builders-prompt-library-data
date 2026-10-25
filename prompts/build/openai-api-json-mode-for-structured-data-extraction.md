---
title: "OpenAI API: JSON Mode for Structured Data Extraction"
slug: openai-api-json-mode-for-structured-data-extraction
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openai-api-json-mode-for-structured-data-extraction
---
# OpenAI API: JSON Mode for Structured Data Extraction

Develop a Python script utilizing OpenAI's JSON Mode to programmatically parse unstructured project inquiries into validated JSON objects.

## Prompt

As a backend developer, you need to extract structured data from unstructured text for a lead generation system. The text is a user's project inquiry.

Your task is to write a Python script that uses the OpenAI API's JSON Mode to parse the inquiry and return a structured JSON object.

**Input Text:**
"Hi, I'm looking to build a new e-commerce website for my clothing brand, 'Retro Threads'. We need a full-stack solution, probably using React for the frontend and Django for the backend. Our budget is around $15,000 and we'd like to launch by the end of Q4 this year. My name is Sarah and my email is sarah@retrothreads.com."

**Desired JSON Structure:**
```json
{
  "contact_name": "Sarah",
  "email": "sarah@retrothreads.com",
  "project_type": "e-commerce website",
  "company_name": "Retro Threads",
  "tech_stack": ["React", "Django"],
  "budget": 15000,
  "timeline": "end of Q4"
}
```

**Technical Requirements:**
- Use the 'openai' Python library with a model that supports JSON mode (e.g., 'gpt-5').
- The API call must set `response_format={"type": "json_object"}`.
- The system message must clearly instruct the model to act as a data extraction expert and to return a JSON object that strictly adheres to the specified structure.
- The script should parse the JSON response and print the resulting Python dictionary to the console.
- Include error handling for invalid JSON output or API failures.

**Output Format:**
A complete, executable Python script.
