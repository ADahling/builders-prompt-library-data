---
title: "Draft a Technical Specification for a New Feature"
slug: draft-a-technical-specification-for-a-new-feature
stage: Design
category: "Documentation"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/draft-a-technical-specification-for-a-new-feature
---
# Draft a Technical Specification for a New Feature

Generate a comprehensive Markdown technical specification for a new feature to align engineering teams on requirements and implementation details.

Variables: feature_name, application_name, user_problem, proposed_solution

## Prompt

You are a product manager who needs to write a detailed technical specification for a new feature, "{{feature_name}}", for your application, {{application_name}}. This document will be used by the engineering team to implement the feature, so it needs to be clear, comprehensive, and unambiguous.

Your task is to generate a technical specification that includes the following sections:

*   **Introduction:** A brief overview of the feature and the problem it solves.
*   **Goals and Non-Goals:** A clear statement of what the feature will and will not do.
*   **User Stories:** A list of user stories that describe how different types of users will interact with the feature.
*   **Technical Design:** A detailed description of the proposed technical implementation, including any changes to the data model, API endpoints, and user interface.
*   **Acceptance Criteria:** A set of measurable criteria that will be used to determine whether the feature has been implemented correctly.
*   **Open Questions:** A list of any open questions or unresolved issues that need to be addressed before development can begin.

Here is some information about the feature:

*   **Feature Name:** {{feature_name}}
*   **User Problem:** {{user_problem}}
*   **Proposed Solution:** {{proposed_solution}}

Generate the complete technical specification in Markdown format. The document should be detailed enough for an engineer to start working on the feature with minimal clarification.
