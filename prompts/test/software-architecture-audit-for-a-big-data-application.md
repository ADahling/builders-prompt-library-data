---
title: "Software Architecture Audit for a Big Data Application"
slug: software-architecture-audit-for-a-big-data-application
stage: Test
category: "Quality Audits"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/software-architecture-audit-for-a-big-data-application
---
# Software Architecture Audit for a Big Data Application

Conduct a comprehensive technical evaluation of big data systems to identify scalability bottlenecks and create a strategic evolution roadmap.

Variables: project_name, project_description, architecture_style, tech_stack

## Prompt

As a principal software architect, I require a comprehensive architecture audit of our big data application, `{{project_name}}`. This system is a {{project_description}} and has evolved over several years. We need to assess its current architectural health and identify areas for improvement to ensure it remains scalable, maintainable, and aligned with our business goals. The current architecture is based on {{architecture_style}} and the tech stack includes {{tech_stack}}.

Your audit should provide a deep analysis of the following architectural aspects:

1.  **Architectural Design and Patterns:**
    *   Evaluate the overall architectural design and its suitability for the application's functional and non-functional requirements.
    *   Assess the consistency and correctness of the implementation of architectural patterns.
    *   Identify any architectural drift or deviations from the intended design.

2.  **Scalability and Performance:**
    *   Analyze the system's ability to handle increasing load and data volume.
    *   Identify any architectural bottlenecks that could limit scalability.
    *   Evaluate the effectiveness of the current scaling strategies.

3.  **Modularity and Coupling:**
    *   Assess the modularity of the system and the level of coupling between its components.
    *   Identify any areas where high coupling could hinder independent development, testing, and deployment.
    *   Provide recommendations for improving modularity and reducing coupling.

4.  **Resilience and Fault Tolerance:**
    *   Review the system's resilience to failures and its ability to recover from them.
    *   Assess the implementation of fault tolerance mechanisms.

5.  **Security:**
    *   Conduct a high-level review of the architectural security. Identify any potential security vulnerabilities at the architectural level.

6.  **Technology Stack and Tooling:**
    *   Evaluate the appropriateness of the current technology stack and development tools.
    *   Identify any outdated or unsupported technologies that should be replaced.

**Output Format:**

Please deliver the architecture audit report in a well-structured Markdown document with the following sections:

*   **Architecture Overview:** A brief description of the current architecture.
*   **Strengths and Weaknesses:** A summary of the key strengths and weaknesses of the current architecture.
*   **Detailed Architectural Findings:** A comprehensive list of all identified architectural issues and areas for improvement. Each finding should include:
    *   **Finding ID:** A unique identifier.
    *   **Architectural Concern:** (e.g., Scalability, Maintainability, Security)
    *   **Description:** A detailed explanation of the issue.
    *   **Impact:** The potential impact of the issue on the system.
    *   **Recommendation:** A clear and actionable recommendation for addressing the issue.
*   **Architectural Roadmap:** A high-level roadmap for evolving the architecture to address the identified issues and meet future requirements.

Your report should provide us with a clear understanding of the state of our architecture and a strategic plan for its evolution.
