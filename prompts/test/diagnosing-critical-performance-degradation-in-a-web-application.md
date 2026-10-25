---
title: "Diagnosing Critical Performance Degradation in a Web Application"
slug: diagnosing-critical-performance-degradation-in-a-web-application
stage: Test
category: "Critical Bugs"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/diagnosing-critical-performance-degradation-in-a-web-application
---
# Diagnosing Critical Performance Degradation in a Web Application

Get a step-by-step performance audit plan for a severe web app slowdown, including triage, key metrics, and frontend analysis.

Variables: app_name, frontend_framework, backend_framework, database_type

## Prompt

Our web application, {{app_name}}, has recently experienced a severe and critical performance degradation. Pages that used to load in under 2 seconds are now taking over 15 seconds to become interactive. This is leading to a high user bounce rate and is impacting our business. The application has a {{frontend_framework}} frontend and a {{backend_framework}} backend, connected to a {{database_type}} database.

As a full-stack performance engineer, you are tasked with leading the investigation to diagnose the root cause of this slowdown. Your response should be a comprehensive, step-by-step performance audit plan.

1.  **Initial Triage and Scoping:**
    *   What are the first questions you would ask to understand the scope of the problem? (e.g., When did it start? Does it affect all users/pages? Any recent deployments?)
    *   What tools would you use for an initial, high-level assessment of the performance problem? Discuss using browser-based tools like Google PageSpeed Insights and WebPageTest. What key metrics would you focus on (e.g., Time to First Byte (TTFB), First Contentful Paint (FCP), Time to Interactive (TTI))?

2.  **Frontend Performance Analysis:**
    *   Outline a detailed plan to analyze the frontend performance using Chrome DevTools.
    *   **Network Panel:** How would you use the Network panel to identify bottlenecks? Discuss looking for large, unoptimized assets (images, JS, CSS), long chains of requests, and slow API responses.
    *   **Performance Panel:** How would you use the Performance panel to profile the application's runtime performance? Explain how to record a profile, and what to look for in the flame chart (e.g., long tasks, layout thrashing, excessive re-renders).
    *   **Lighthouse:** How would you use the Lighthouse audit to get a prioritized list of frontend performance issues to address?

3.  **Backend Performance Analysis:**
    *   The frontend analysis reveals that the TTFB is very high, suggesting a backend problem. Outline a plan to investigate the backend.
    *   **APM (Application Performance Monitoring):** Explain the role of an APM tool (like New Relic, Datadog, or Sentry). If you had an APM, what dashboards and traces would you look at to find the slow transaction?
    *   **Logging:** In the absence of an APM, how would you use structured logging to find the bottleneck? Provide an example of how you would add timing information to your logs for a specific API endpoint to measure the duration of different parts of the request (e.g., database queries, external API calls).

4.  **Database Performance Analysis:**
    *   The backend investigation points to a slow database query. The query that used to be fast is now taking several seconds.
    *   What are the most common reasons for a sudden database query slowdown? (e.g., missing indexes, outdated statistics, parameter sniffing, table growth).
    *   Explain how you would use the database's query execution plan ('EXPLAIN PLAN' in SQL) to understand how the database is running the query and to identify the performance issue (e.g., a full table scan instead of an index seek).
    *   Propose a fix for a slow query, such as adding a specific index. Explain how to write the 'CREATE INDEX' statement and why it would help.

5.  **Resolution and Long-Term Monitoring:**
    *   Once the root cause is identified and fixed, what is the process for deploying the fix safely?
    *   What long-term performance monitoring and alerting should be set up to prevent this from happening again? Define specific performance budgets (e.g., TTFB < 200ms, TTI < 3s) and explain how you would configure alerts to be notified if these budgets are violated.

Your response should be a detailed and professional plan of at least 600 words, demonstrating a systematic approach to performance engineering.
