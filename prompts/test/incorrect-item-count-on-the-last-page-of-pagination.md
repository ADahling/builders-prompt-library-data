---
title: "Incorrect Item Count on the Last Page of Pagination"
slug: incorrect-item-count-on-the-last-page-of-pagination
stage: Test
category: "Functional Bugs"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/incorrect-item-count-on-the-last-page-of-pagination
---
# Incorrect Item Count on the Last Page of Pagination

Fix the paginated SQL query logic to ensure the final page returns the correct remaining item count instead of the full page size.

Variables: project_name, backend_framework, database_name

## Prompt

You are a backend developer for {{project_name}}. The API that provides paginated data has a bug in its calculation. For every page, it returns a full 10 items, even on the last page where there might only be 3 items left. For example, if there are 23 items in total and the page size is 10, page 3 should return 3 items, but the API is incorrectly returning 10 (possibly by grabbing items from the previous page or returning duplicates).

Your task is to fix the database query on the backend to correctly calculate the `LIMIT` and `OFFSET` for the last page.

**Context:**
- **Backend:** {{backend_framework}} API.
- **Database:** A SQL database like {{database_name}}.
- **Parameters:** The API endpoint receives `page` and `pageSize` as inputs.

**Buggy SQL Query Logic:**

```javascript
// Assuming page is 1-indexed
const pageSize = 10;
const offset = (page - 1) * pageSize;

// The LIMIT is always fixed, which is the source of the bug.
const limit = pageSize;

const query = `SELECT * FROM items ORDER BY created_at DESC LIMIT ${limit} OFFSET ${offset}`;
```

**Instructions:**

1.  **Analyze the Query Bug:** Explain how a fixed `LIMIT` can cause incorrect data to be returned on the final page, especially if the total number of items is not a multiple of the page size.
2.  **Implement Correct Calculation:** Your solution requires knowing the total number of items. You will need to perform a `COUNT(*)` query first. Then, when calculating the `LIMIT` and `OFFSET

## Tips

A common backend pagination bug that requires careful SQL query construction.
