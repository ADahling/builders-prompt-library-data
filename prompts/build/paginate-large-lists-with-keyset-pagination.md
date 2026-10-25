---
title: "Paginate large lists with keyset pagination"
slug: paginate-large-lists-with-keyset-pagination
stage: Build
category: "Database & Supabase"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/paginate-large-lists-with-keyset-pagination
---
# Paginate large lists with keyset pagination

Replace offset queries with keyset pagination using stable ordering, matching indexes, safe cursors, and explicit rules for new rows.

Variables: schema_definition, current_query_code, pagination_requirements

## Prompt

You are a PostgreSQL and Supabase engineer implementing keyset pagination.

Context:
- Schema, indexes, and RLS policies: {{schema_definition}}
- Current query and pagination code: {{current_query_code}}
- List behavior, filters, and sorting requirements: {{pagination_requirements}}

Your task is to replace offset pagination with stable cursors and indexed queries for both directions.

Steps:
1. Map filters and ORDER BY. Choose stable sort columns plus a unique tie breaker. Check nulls, timestamp precision, and mutable sort values. State the complete order.
2. Write first and next page SQL using LIMIT page_size + 1. Use tuple comparisons for uniform directions, such as (created_at, id) < ($1, $2) for descending order. Expand mixed directions into lexicographic OR predicates. Handle nulls explicitly.
3. Write previous page SQL from the first displayed row. Invert the comparison and ORDER BY, trim the extra row, then reverse results for display. Derive cursors from displayed boundary rows. Explain which availability flag the extra row proves and how to check the other.
4. Define a versioned base64url cursor containing all sort values and filter scope. Preserve database precision. Validate types, scope, version, and size. Show encode and decode code; distinguish encoding from signing and authorization.
5. Provide CREATE INDEX SQL matching equality filters, sort columns, and directions. Check partial index predicates. Show EXPLAIN (ANALYZE, BUFFERS) checks for deep pages, unwanted sorts, and excessive row scans.
6. Show Supabase query or RPC integration with bounded page sizes. Define live feed versus frozen membership behavior. Explain inserts, deletes, and sort updates; a high water mark does not freeze backdated inserts or updates. Cover tied keys, empty pages, backward travel, malformed cursors, and concurrent writes in test cases.

Constraints:
- Do not invent project facts. List assumptions and missing details.
- Preserve filters, tenant boundaries, and RLS. Never trust cursor values as authorization.
- Use bound SQL values. Avoid OFFSET and client side full list sorting.

Output format, in Markdown: Assumptions, Ordering and cursor contract, SQL and indexes, Integration code, Concurrent changes, and a Test cases table.

## Tips

Paste table definitions, existing indexes, and the query code that loads the list. Include active filters, sort options, and whether new rows should appear during scrolling.
