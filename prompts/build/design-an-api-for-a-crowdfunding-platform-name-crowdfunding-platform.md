---
title: "Design an API for a Crowdfunding Platform"
slug: design-an-api-for-a-crowdfunding-platform-name-crowdfunding-platform
stage: Build
category: "API Design"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-crowdfunding-platform-name-crowdfunding-platform
---
# Design an API for a Crowdfunding Platform

Get a REST API design for crowdfunding, with endpoints and request/response formats for project management, browsing, pledges, payments, and rewards.

Variables: crowdfunding_platform_name

## Prompt

I am building a crowdfunding platform called {{crowdfunding_platform_name}}, similar to Kickstarter or Indiegogo. I need to design the API for it.

Your task is to design the core API for the platform.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the platform (e.g., projects, creators, backers, pledges, rewards).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Creators can create and manage projects.
    *   Backers can browse projects and make pledges.
    *   The platform handles payments and rewards fulfillment.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoint, including the HTTP method, URI, and request/response format.
