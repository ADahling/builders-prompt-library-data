---
title: "Fix Search Highlighting That Breaks HTML Structure"
slug: fix-search-highlighting-that-breaks-html-structure
stage: Test
category: "Functional Bugs"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-search-highlighting-that-breaks-html-structure
---
# Fix Search Highlighting That Breaks HTML Structure

Implement robust search term highlighting that preserves HTML integrity and prevents document structure breakage.

Variables: project_name

## Prompt

You are a developer for {{project_name}}. The search results page has a feature that highlights the search term within the results. The current implementation uses a simple string `replace` with a `<mark>` tag, like `result.text.replace(query, '<mark>${query}</mark>')`. This has a critical bug: if the search result text itself contains HTML, this simple replacement can break the HTML structure, leading to a broken layout or even a React render error.

For example, if the text is `"This is a <b>bold</b> term"` and the query is `"a bold term"

## Tips

A very tricky front-end bug that requires a deep understanding of the DOM and how to manipulate it safely.
