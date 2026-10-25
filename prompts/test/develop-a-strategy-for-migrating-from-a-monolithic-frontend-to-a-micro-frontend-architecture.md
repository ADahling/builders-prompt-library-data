---
title: "Develop a Strategy for Migrating from a Monolithic Frontend to a Micro-frontend Architecture"
slug: develop-a-strategy-for-migrating-from-a-monolithic-frontend-to-a-micro-frontend-architecture
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/develop-a-strategy-for-migrating-from-a-monolithic-frontend-to-a-micro-frontend-architecture
---
# Develop a Strategy for Migrating from a Monolithic Frontend to a Micro-frontend Architecture

Your company's frontend is a large, monolithic single-page application managed in one repository.

Variables: framework

## Prompt

My company's frontend is a large, monolithic `{{framework}}` application managed in a single repository. It has become slow to build, difficult to deploy, and different teams are constantly stepping on each other's toes. We want to migrate to a micro-frontend architecture to enable independent development and deployment.

Your task is to create a high-level strategic plan for this migration.

1.  **Micro-frontend Architecture Explained:** Start by explaining the concept of micro-frontends. What are the benefits (e.g., autonomous teams, independent deployments, technology flexibility) and the challenges (e.g., operational complexity, shared component management)?
2.  **Composition Strategy:** How will the different micro-frontends be composed together into a single, seamless user experience? Compare different composition strategies:
    *   **Build-time composition** (e.g., using NPM packages).
    *   **Server-side composition** (e.g., using Server-Side Includes).
    *   **Client-side composition** (e.g., using a container application and a framework like `single-spa` or Webpack 5's Module Federation).
    Recommend one strategy and justify your choice for our `{{framework}}` application.
3.  **Migration Plan:** Propose an incremental migration plan. We can't do this all at once. 
    *   How do we choose the first part of the monolith to extract into a micro-frontend?
    *   How does the new micro-frontend communicate with the existing monolith (e.g., via a shared event bus, custom events)?
    *   How do we handle shared components, styling, and user authentication across the micro-frontends?
4.  **Tooling and Infrastructure:** What new tooling and infrastructure will be required? (e.g., a separate CI/CD pipeline for each micro-frontend, a shared component library, a design system).

Output should be a strategic document that can be presented to engineering leadership.

## Tips

Micro-frontends are a major architectural shift. This prompt tackles the strategic planning required for such a move.
