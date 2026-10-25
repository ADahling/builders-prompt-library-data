---
title: "Apply Domain-Driven Design to a Greenfield Project"
slug: apply-domain-driven-design-to-a-greenfield-project
stage: Build
category: "System Architecture"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/apply-domain-driven-design-to-a-greenfield-project
---
# Apply Domain-Driven Design to a Greenfield Project

Guide a team through implementing Domain-Driven Design for a new project, from strategic event storming to tactical code implementation.

Variables: project_description, programming_language

## Prompt

You are a senior software architect and a proponent of Domain-Driven Design (DDD). Our team is about to start a new greenfield project, a {{project_description}}, and we want to apply DDD principles from the very beginning.

**Your Task:**
Create a practical guide for our team on how to get started with DDD for this project. The guide should be easy to understand for developers who are new to DDD.

**Instructions & Constraints:**
1.  **Introduction to DDD:**
    *   Provide a brief, developer-friendly introduction to the core concepts of DDD: Ubiquitous Language, Bounded Contexts, Aggregates, Entities, and Value Objects.
    *   Explain the difference between Strategic Design and Tactical Design.

2.  **Strategic Design Workshop:**
    *   Outline a plan for a workshop with domain experts to kick off the project. This is often called an "Event Storming" session.
    *   Describe the goals of the workshop, who should be involved, and what the agenda should look like.
    *   Explain how to use the workshop to identify the core domains, subdomains, and the Ubiquitous Language.

3.  **Defining Bounded Contexts:**
    *   Guide the team on how to use the insights from the workshop to define the Bounded Contexts for the application.
    *   Explain how to create a Context Map to visualize the relationships between the different Bounded Contexts.

4.  **Tactical Design First Steps:**
    *   Provide a step-by-step guide for the team to start with the tactical design within a single Bounded Context.
    *   Show how to identify Aggregates, Entities, and Value Objects.
    *   Give a simple code example in {{programming_language}} that illustrates how to structure the code according to DDD principles (e.g., separating the domain layer from the application and infrastructure layers).

**Output Format:**
Present the information in a clear and concise Markdown document, structured as follows:
1.  **A Developer's Introduction to Domain-Driven Design**
2.  **Planning Your Strategic Design Workshop (Event Storming)**
3.  **From Workshop to Bounded Contexts: A Practical Guide**
4.  **Getting Started with Tactical Design: Your First Aggregate**
