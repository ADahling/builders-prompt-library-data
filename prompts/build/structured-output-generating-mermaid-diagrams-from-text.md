---
title: "Structured Output: Generating Mermaid Diagrams from Text"
slug: structured-output-generating-mermaid-diagrams-from-text
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-generating-mermaid-diagrams-from-text
---
# Structured Output: Generating Mermaid Diagrams from Text

Transform natural language system descriptions into valid Mermaid.js flowchart code for automated architectural visualization.

## Prompt

You are building a documentation tool that automatically visualizes system architecture from a textual description. You will use an LLM to convert the description into Mermaid.js syntax, which can then be rendered into a diagram.

Your task is to create a prompt for an LLM to perform this translation.

**Scenario:**
- **User Request:** "I have a simple web service. A user's browser sends an HTTPS request to our Load Balancer. The Load Balancer forwards the request to one of three Web Servers. Each Web Server can query a central PostgreSQL Database."
- **Desired Mermaid Output:**
`graph TD
    A[User Browser] --> B{Load Balancer}
    B --> C1[Web Server 1]
    B --> C2[Web Server 2]
    B --> C3[Web Server 3]
    C1 --> D[(PostgreSQL Database)]
    C2 --> D
    C3 --> D`

**Prompt Engineering Task:**
You are not writing code, but the prompt itself.

**Prompt Requirements:**
1.  **Role Definition:** "You are an expert system architect and a specialist in creating diagrams using Mermaid.js syntax."
2.  **The Task:** "Your task is to convert the following description of a system architecture into a valid Mermaid.js flowchart diagram (`graph TD`)."
3.  **Input Data:** Provide the user's request text.
4.  **Constraints:**
    -   "Identify the key components (nodes) and the connections between them (edges)."
    -   "Use appropriate shapes for different components (e.g., a diamond for a load balancer, a database shape for the database)."
    -   "The output must be a single block of valid Mermaid.js code. Do not include any extra text, explanations, or markdown code fences (like `mermaid`)."

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the LLM.
