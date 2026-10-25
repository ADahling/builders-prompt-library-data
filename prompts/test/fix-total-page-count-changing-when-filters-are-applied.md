---
title: "Fix Total Page Count Changing When Filters Are Applied"
slug: fix-total-page-count-changing-when-filters-are-applied
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-total-page-count-changing-when-filters-are-applied
---
# Fix Total Page Count Changing When Filters Are Applied

Synchronize pagination state with filtering logic to ensure total page counts and current page indices update correctly after data resets.

Variables: project_name, frontend_framework

## Prompt

You are a developer for {{project_name}}, an e-commerce site. The product list page has both pagination and filtering (e.g., by category, price range). There is a bug: a user is on page 2 of 10 total pages. They then apply a filter that reduces the total number of products, so there should now only be 3 total pages. However, the pagination control still shows "Page 2 of 10", which is now incorrect and confusing.

This happens because applying a filter triggers a re-fetch of the page's data, but the component does not reset the current page number or correctly update the total page count.

**Context:**
- **Features:** Pagination and filtering working together.
- **Problem:** State is not correctly synchronized between the two features.

**Instructions:**

1.  **Analyze the State Synchronization Bug:** Explain how the state of the filters and the state of the pagination are related. Describe the race condition or state management flaw where changing the filters doesn't correctly trigger a reset of the pagination state.
2.  **Implement a State Reset on Filter Change:** In your {{frontend_framework}} component, use a `useEffect` hook that has the filter values as dependencies. When any of these filter values change, this hook should be triggered, and it must reset the current page number back to 1 before fetching the new data.
3.  **Ensure Total Pages is Updated:** The API response for the filtered data must include the new, correct `totalPages` count. Your component must update its `totalPages` state with this new value, ensuring the pagination controls (e.g., "Page X of Y") are accurate.

**Output Format:**

- **State Bug Analysis:** A clear explanation of the synchronization problem.
- **Component Code with Reset Logic:** The complete, corrected component code showing the `useEffect` hook that resets the page number when filters change.

## Tips

A common bug when combining multiple stateful UI features. Teaches the importance of state synchronization.
