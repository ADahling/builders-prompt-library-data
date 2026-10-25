---
title: "Structured Output: Extracting Knowledge Graphs with Gemini"
slug: structured-output-extracting-knowledge-graphs-with-gemini
stage: Build
category: "LLM & AI Integration"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-extracting-knowledge-graphs-with-gemini
---
# Structured Output: Extracting Knowledge Graphs with Gemini

Generate a Python script using the Gemini API and response_schema to extract factual relations from text into a structured JSON knowledge graph.

## Prompt

You are building a research tool that automatically constructs knowledge graphs from scientific papers. You need the LLM to extract entities (nodes) and their relationships (edges) in a strict, predictable format.

Your task is to write a Python script using the Google Gemini API to extract a knowledge graph from a short text snippet using the `response_schema` feature.

**Scenario:**
- **Input Text:** "Albert Einstein was born in Ulm, Germany. He developed the theory of relativity. He worked at the Institute for Advanced Study in Princeton."

**Technical Requirements:**
- Use the 'google-generativeai' library and the Gemini 3 model.
- Define a strict JSON schema for the output. The schema should represent a list of "Relationships". Each relationship should have:
    - `subject` (string, e.g., "Albert Einstein")
    - `predicate` (string, e.g., "born in")
    - `object` (string, e.g., "Ulm, Germany")
- Pass this schema to the `generation_config` parameter using `response_mime_type="application/json"` and `response_schema=your_schema`.
- The prompt should instruct the model to extract all factual relationships from the text and format them according to the schema.
- Print the resulting JSON string to the console.

**Output Format:**
A complete Python script demonstrating strict structured output generation with Gemini.
