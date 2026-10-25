---
title: "Design an API for a Charity Donation Platform"
slug: design-an-api-for-a-charity-donation-platform-name-charity-donation-platform
stage: Build
category: "API Design"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-charity-donation-platform-name-charity-donation-platform
---
# Design an API for a Charity Donation Platform

Get a REST API design for a charity platform, with endpoints and request/response formats for charity searches, donations, and donation history.

Variables: charity_donation_platform_name

## Prompt

I am building a charity donation platform called {{charity_donation_platform_name}}. I need to design the API for it.

Your task is to design the core API for the platform.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the platform (e.g., charities, users, donations, campaigns).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   Users can browse and search for charities.
    *   Users can make donations to charities or specific campaigns.
    *   The platform tracks donation history.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoint, including the HTTP method, URI, and request/response format.
