---
title: "Pagination State Lost on Page Reload or Navigation"
slug: pagination-state-lost-on-page-reload-or-navigation
stage: Test
category: "Functional Bugs"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/pagination-state-lost-on-page-reload-or-navigation
---
# Pagination State Lost on Page Reload or Navigation

Implement persistent pagination by synchronizing component state with URL query parameters to maintain position during navigation.

Variables: project_name, frontend_framework

## Prompt

You are a developer for {{project_name}}. A user navigates to page 3 of a product list, clicks on a product to view its details, and then uses the browser's back button to return to the list. The user expects to be on page 3, but the application has reset and is showing page 1. The pagination state is not being preserved.

Your task is to fix this by synchronizing the current page number with the URL's query parameters.

**Context:**
- **Framework:** {{frontend_framework}} with a routing library (e.g., React Router, Vue Router).
- **Problem:** The current page state is stored only in the component's local state, which is lost on navigation.

**Instructions:**

1.  **Explain the State Loss Problem:** Describe why component state is ephemeral and how storing application state in the URL makes the UI more robust and shareable.
2.  **Read Page from URL on Load:** Modify the component to read the page number from the URL query parameter (e.g., `?page=3`) when it first mounts. If the parameter is not present, it should default to page 1.
3.  **Update URL on Page Change:** When the user clicks the "Next", "Previous", or a specific page number button, you must not only update the component's state but also programmatically update the URL's query parameter to reflect the new page number. Use the `useHistory` or `useRouter` hook from your routing library to achieve this.

**Output Format:**

- **State Loss Analysis:** A clear explanation of the problem.
- **Refactored Component Code:** The complete code for the component that reads from and writes to the URL query parameters to manage the pagination state.

## Tips

A crucial UX improvement that teaches how to create persistent and shareable URLs.
