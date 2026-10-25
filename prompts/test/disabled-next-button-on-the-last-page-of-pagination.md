---
title: "Disabled Next Button on the Last Page of Pagination"
slug: disabled-next-button-on-the-last-page-of-pagination
stage: Test
category: "Functional Bugs"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/disabled-next-button-on-the-last-page-of-pagination
---
# Disabled Next Button on the Last Page of Pagination

Disable the pagination "Next" button on the final page to prevent redundant API calls and improve the user experience.

Variables: project_name, tech_stack

## Prompt

You are a front-end developer for {{project_name}}. The application has a paginated list of items. A bug has been reported: the "Next" button in the pagination controls remains active even when the user is on the very last page. Clicking it results in an unnecessary API request for a page that doesn't exist, which returns an empty array and confuses the user.

Your task is to correctly disable the "Next" button when the user reaches the last page.

**Context:**
- **API Response:** The API returns the data for the current page along with pagination metadata. A common pattern is:
  ```json
  {
    "data": [ ... ],
    "pagination": {
      "currentPage": 3,
      "totalPages": 5,
      "totalItems": 48
    }
  }
  ```
- **Frontend:** A {{tech_stack}} component that manages the pagination state.

**Instructions:**

1.  **Identify the Missing Logic:** Explain that the component is not using the `totalPages` (or equivalent) metadata from the API to determine if it's on the last page.
2.  **Implement the Disabling Logic:** In the component that renders the pagination controls, add a condition to disable the "Next" button. The condition should be `currentPage === totalPages`.
3.  **Provide the Corrected Component:** Show the refactored component code, including the state management for `currentPage` and `totalPages

## Tips

A fundamental pagination bug that every junior developer should be able to solve.
