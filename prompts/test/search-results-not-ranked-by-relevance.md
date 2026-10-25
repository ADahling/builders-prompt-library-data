---
title: "Search Results Not Ranked by Relevance"
slug: search-results-not-ranked-by-relevance
stage: Test
category: "Functional Bugs"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/search-results-not-ranked-by-relevance
---
# Search Results Not Ranked by Relevance

Implement TF-IDF based relevance ranking in PostgreSQL or Elasticsearch to ensure search results are ordered by topical importance.

Variables: project_name, search_term, database_name

## Prompt

You are a search engineer for {{project_name}}. The current search functionality returns results in a seemingly random or chronological order. A search for "{{search_term}}" might return an article where the term is mentioned once in a footnote before an article where it is the main topic. Users expect the most relevant results to appear first.

Your task is to implement relevance ranking for your search results using a full-text search engine.

**Context:**
- **Search Engine:** A full-text search capable database like {{database_name}} (PostgreSQL, Elasticsearch).
- **Problem:** Search results lack relevance scoring.

**Instructions:**

1.  **Explain Relevance Ranking:** Briefly describe the concepts behind search relevance, such as TF-IDF (Term Frequency-Inverse Document Frequency). Explain why it’s important to rank documents based on how often a search term appears and how unique that term is across all documents.
2.  **Implement Ranking in Your Query:** Modify your full-text search query to calculate a relevance score for each result and order the results by that score in descending order.
    *   **For PostgreSQL:** Show how to use `ts_rank` or `ts_rank_cd` to calculate the score and use it in the `ORDER BY` clause.
    *   **For Elasticsearch:** Explain how relevance scoring is built-in by default (`_score`) and how you can influence it with different query types (e.g., `bool` query with `should` clauses).
3.  **Provide the Ranked Query:** Give the complete query that returns results ordered by relevance.

**Output Format:**

- **Relevance Ranking Explanation:** A summary of the concept.
- **Ranked Search Query:** The complete query that includes relevance scoring and ordering.

## Tips

The next step after implementing basic FTS. Ranking is key to a good search experience.
