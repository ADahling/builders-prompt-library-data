---
title: "Add ranked full-text search to a table"
slug: add-ranked-full-text-search-to-a-table
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/add-ranked-full-text-search-to-a-table
---
# Add ranked full-text search to a table

Build ranked Postgres full-text search with weighted fields, highlighted snippets, typo fallback, and SQL suited to your schema.

Variables: schema_definition, search_requirements, existing_search_code

## Prompt

You are a Postgres engineer building ranked search for Supabase.

Context:
- Table DDL, indexes, grants, and RLS policies: {{schema_definition}}
- Search fields, language, priorities, and behavior requirements: {{search_requirements}}
- Existing search SQL or application code, if any: {{existing_search_code}}

Your task is to add ranked full-text search with snippets and a bounded fallback.

Steps:
1. Map fields to A through D weights. Choose an explicit regconfig and use it consistently for indexing, parsing, and snippets. List assumptions for missing requirements.
2. Write a migration adding a GENERATED ALWAYS AS STORED tsvector using setweight, coalesce, and vector concatenation, plus a GIN index. Use immutable expressions and explicit regconfig casts. Flag rewrite and lock costs; keep CREATE INDEX CONCURRENTLY outside transactions.
3. Parse bound input once with websearch_to_tsquery. Filter with @@, rank with ts_rank_cd and explicit weights, and break ties with a unique key. Bound result counts. Use a SECURITY INVOKER RPC if needed; preserve RLS and check grants.
4. Apply ts_headline only to limited matches. Set snippet length and markers. Treat its output as untrusted: require safe rendering, not raw HTML insertion.
5. Handle null fields, blank or stopword-only input, punctuation, short queries, misspellings, and zero matches. Define fallback triggers and limits. Use pg_trgm with an index-supported % predicate, then similarity ranking. Address weak trigram matching for very short input with a bounded prefix path or minimum length. Avoid unbounded scans.
6. Provide checks for ranking, language, fallback, ties, RLS, and snippet injection. Include EXPLAIN (ANALYZE, BUFFERS) queries for a safe environment. Flag unverified behavior, extension availability, and performance; list next steps.

Constraints:
- Do not invent project facts. List assumptions.
- Bind query values; never concatenate user SQL.
- Do not disable RLS or bypass it for fallback.
- Do not claim checks ran without evidence.

Output format, in Markdown: Assumptions first, then Migration SQL, Search SQL and Integration, Checks as a table with columns case, check, expected result, then Unverified Items and Next Steps.

If the full answer does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Paste table DDL, RLS policies, and any current search SQL or Supabase RPC code. Include searchable fields, language, ranking priorities, and expected query examples.
