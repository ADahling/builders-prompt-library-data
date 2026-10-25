---
title: "Fix Unstable Pagination with Items Added/Deleted During Browsing"
slug: fix-unstable-pagination-with-items-added-deleted-during-browsing
stage: Test
category: "Functional Bugs"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-unstable-pagination-with-items-added-deleted-during-browsing
---
# Fix Unstable Pagination with Items Added/Deleted During Browsing

Refactor a dynamic feed's pagination from offset-based to cursor-based to eliminate duplicate or missed items during real-time updates.

Variables: project_name

## Prompt

You are a developer working on a real-time feed in {{project_name}}, where new items can be added to the top of the list while a user is paginating through older items. This causes an issue with traditional offset-based pagination: if a user is on page 2 (items 11-20) and 5 new items are added to the list, when they navigate to page 3, they will see items 21-30 of the *new* list. This means they will miss 5 items and may even see duplicates.

Your task is to refactor the pagination from an offset-based approach to a more stable cursor-based (or keyset) pagination.

**Context:**
- **Problem:** Offset-based pagination is not stable on a dataset that changes frequently.

**Instructions:**

1.  **Explain the Instability of Offset Pagination:** Clearly illustrate with an example how adding or deleting items from a list breaks offset-based pagination, leading to skipped or repeated items.
2.  **Design a Cursor-Based Pagination Strategy:** Describe how cursor-based pagination works. Instead of a page number, the client asks for items "after" a specific, unique identifier from the last item on the current page (e.g., `?limit=10&after=item_id_20`). The unique identifier should be on a column that is sequential and indexed (like a timestamp or a unique serial ID).
3.  **Provide Backend and Frontend Implementation:**
    *   **Backend:** Show the new backend endpoint logic. It should accept an `after` cursor. The SQL query will now use a `WHERE` clause (e.g., `WHERE created_at < :cursor`) instead of an `OFFSET`.
    *   **Frontend:** Show how the frontend component will now store the cursor of the last item and send it in the request for the next page.

**Output Format:**

- **Offset Instability Analysis:** A detailed explanation of the problem.
- **Cursor-Based Strategy Design:** A description of the cursor-based approach.
- **Backend and Frontend Code:** The code snippets for both the backend API and the frontend component to implement cursor-based pagination.

## Tips

The definitive solution for stable pagination in dynamic datasets. A must-know for real-time applications.
