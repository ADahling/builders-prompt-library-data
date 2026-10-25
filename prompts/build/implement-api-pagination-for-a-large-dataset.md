---
title: "Implement API Pagination for a Large Dataset"
slug: implement-api-pagination-for-a-large-dataset
stage: Build
category: "API Design"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-api-pagination-for-a-large-dataset
---
# Implement API Pagination for a Large Dataset

Compare offset and cursor pagination with code examples, a trade-off table, and a recommendation for a real-time feed with frequent new items.

## Prompt

I have an API endpoint that returns a large list of items, and I need to implement pagination to improve performance and reduce the payload size. 

Your task is to explain and compare different pagination strategies and recommend the best one for my use case.

**Instructions:**
1.  **Pagination Strategies:** Describe the following pagination strategies:
    *   Offset/Limit Pagination
    *   Cursor-based Pagination (Keyset Pagination)
2.  **Comparison:** Compare the pros and cons of each strategy. Consider factors like performance, consistency, and ease of implementation.
3.  **Recommendation:** Recommend the best pagination strategy for a real-time feed where new items are frequently added to the beginning of the list. Justify your recommendation.

**Output Format:**
Provide the output as a Markdown document. For each pagination strategy, provide a clear explanation and a code example showing how to implement it. Then, present the comparison in a table. Finally, state your recommendation and the reasons behind it.
