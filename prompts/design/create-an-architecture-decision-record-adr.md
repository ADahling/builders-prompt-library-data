---
title: "Create an Architecture Decision Record (ADR)"
slug: create-an-architecture-decision-record-adr
stage: Design
category: "Documentation"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-architecture-decision-record-adr
---
# Create an Architecture Decision Record (ADR)

Generate a structured Architecture Decision Record in Markdown to document and justify the selection of a specific database technology.

Variables: database_technology, alternative_database_1, alternative_database_2

## Prompt

You are a senior software architect leading a team building a new microservices-based e-commerce platform. You need to document a critical architectural decision to ensure all team members understand the reasoning behind it and to maintain a clear history of architectural choices.

Your task is to create an Architecture Decision Record (ADR) for the decision to use {{database_technology}} as the primary database for the new platform. The ADR should follow a standard template and include the following sections:

*   **Title:** A short, descriptive title for the decision.
*   **Status:** The current status of the decision (e.g., Proposed, Accepted, Deprecated).
*   **Context:** A detailed description of the problem or issue that this decision addresses. What are the technical, business, and operational constraints?
*   **Decision:** A clear and concise statement of the architectural decision that was made.
*   **Consequences:** A thorough analysis of the positive and negative consequences of this decision. This should include the impact on performance, scalability, security, cost, and developer experience.
*   **Alternatives Considered:** A list of the other options that were considered, with a brief explanation of why they were not chosen.

Here is some context for the decision:

*   **Problem:** The team needs to choose a database technology that can handle a high volume of transactional data, support complex queries, and scale horizontally.
*   **Alternatives Considered:** {{alternative_database_1}}, {{alternative_database_2}}

Generate the complete ADR in Markdown format. The content should be well-researched, objective, and provide a clear justification for the chosen solution.
