---
title: "In-Depth Performance Audit and Optimization Plan for a Django Application"
slug: in-depth-performance-audit-and-optimization-plan-for-a-django-application
stage: Test
category: "Quality Audits"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/in-depth-performance-audit-and-optimization-plan-for-a-django-application
---
# In-Depth Performance Audit and Optimization Plan for a Django Application

Generate a comprehensive full-stack performance audit and prioritized optimization roadmap to resolve Django application bottlenecks.

Variables: project_name, project_description, specific_feature, tech_stack

## Prompt

As a seasoned performance engineer, I need you to conduct an in-depth performance audit of our Django web application, `{{project_name}}`. This application is a {{project_description}} and is currently experiencing performance bottlenecks under high traffic, particularly in the {{specific_feature}} module. The tech stack includes {{tech_stack}}.

Your audit must cover the entire application stack, from the frontend to the database. Please analyze the following aspects:

1.  **Frontend Performance:**
    *   Analyze the critical rendering path, identify render-blocking resources, and suggest optimizations.
    *   Evaluate image and asset optimization (compression, formats, delivery).
    *   Assess JavaScript execution time, identify long-running tasks, and recommend code-splitting and lazy loading strategies.
    *   Measure and provide recommendations to improve key performance metrics (FCP, LCP, TTI, CLS).

2.  **Backend Performance:**
    *   Profile the backend code to identify performance hotspots, memory leaks, and inefficient algorithms.
    *   Analyze API response times and identify slow endpoints.
    *   Review caching strategies (in-memory, distributed cache) and suggest improvements.
    *   Assess the efficiency of database queries and identify N+1 query problems.

3.  **Database Performance:**
    *   Analyze slow database queries and suggest indexing strategies.
    *   Review the database schema for design flaws that could impact performance.
    *   Assess connection pooling and configuration.

4.  **Infrastructure and Scalability:**
    *   Review the current infrastructure setup and identify any scalability limitations.
    *   Analyze the application's ability to handle concurrent users and suggest auto-scaling configurations.

**Output Format:**

Provide a comprehensive performance audit report in Markdown format with the following structure:

*   **Performance Scorecard:** A summary of the current performance with scores for each area (Frontend, Backend, Database).
*   **Key Findings and Bottlenecks:** A detailed list of the most critical performance issues discovered.
*   **Actionable Optimization Plan:** A prioritized list of recommendations to address the identified bottlenecks. Each recommendation should include:
    *   **Recommendation ID:** A unique identifier.
    *   **Area:** (Frontend, Backend, Database, Infrastructure)
    *   **Effort:** (Low, Medium, High)
    *   **Impact:** (Low, Medium, High)
    *   **Detailed Steps:** A clear, step-by-step guide on how to implement the optimization, with code examples where applicable.
*   **Projected Performance Improvements:** An estimation of the expected performance gains after implementing the recommendations.

Your report should be detailed, data-driven, and provide a clear roadmap for our development team to follow to improve the application's performance and scalability.
