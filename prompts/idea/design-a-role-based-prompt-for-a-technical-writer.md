---
title: "Design a Role-Based Prompt for a Technical Writer"
slug: design-a-role-based-prompt-for-a-technical-writer
stage: Idea
category: "Prompt Engineering"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-role-based-prompt-for-a-technical-writer
---
# Design a Role-Based Prompt for a Technical Writer

Generate an AI-driven prompt that transforms technical specifications into user-friendly manual sections following professional style guides.

Variables: app_name, feature_name

## Prompt

You are a technical writer tasked with creating a user manual for a new software application called {{app_name}}. Your task is to design a role-based prompt that instructs an AI to act as an expert technical writer and generate a section of the user manual.

The prompt should define the AI's role as a technical writer with the following characteristics:

- **Expertise**: Deep understanding of technical writing principles and best practices.
- **Audience**: Ability to write for a non-technical audience, using clear and simple language.
- **Style**: Adherence to a specific style guide (e.g., Microsoft Manual of Style).

The prompt should also provide the AI with the necessary context, including:

- **Feature**: The specific feature of the application to be documented ({{feature_name}}).
- **User Goal**: What the user wants to achieve by using this feature.
- **Steps**: The steps required to use the feature.

The output should be a well-structured section of the user manual, with a clear title, an introduction, and a step-by-step guide.

## Tips

This prompt uses role-based prompting to generate high-quality technical documentation. By defining the AI's role, you can ensure the output meets specific standards of quality and style.
