---
title: "System Prompt Engineering Framework"
slug: system-prompt-engineering-framework
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-prompt-engineering-framework
---
# System Prompt Engineering Framework

Construct a comprehensive, production-grade system prompt architecture featuring identity definitions, safety guardrails, and testing plans.

Variables: assistant_purpose, target_users, desired_tone, constraints

## Prompt

You are a prompt engineering expert. Design a production-grade system prompt for an AI assistant that {{assistant_purpose}}.

Requirements:
- Target users: {{target_users}}
- Tone: {{desired_tone}}
- Constraints: {{constraints}}

System prompt structure:
1. **Identity & Role**: Who the AI is and what it does (be specific)
2. **Capabilities**: What the AI can do (explicit list)
3. **Limitations**: What the AI cannot or should not do
4. **Response Format**: How to structure responses (markdown, JSON, etc.)
5. **Tone & Style**: Communication style guidelines with examples
6. **Error Handling**: How to respond when unsure or unable to help
7. **Safety Guardrails**: Topics to avoid, harmful content prevention
8. **Context Handling**: How to use conversation history and uploaded files
9. **Tool Usage**: When and how to use available tools
10. **Examples**: 3 example interactions showing ideal behavior

Also provide:
- A/B testing plan for the system prompt
- Evaluation rubric for response quality
- Version control strategy for prompt iterations

## Tips

The system prompt is the most important piece of any AI application. Iterate on it like you would iterate on code.
