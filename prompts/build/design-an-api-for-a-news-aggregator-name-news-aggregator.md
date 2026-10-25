---
title: "Design an API for a News Aggregator"
slug: design-an-api-for-a-news-aggregator-name-news-aggregator
stage: Build
category: "API Design"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-news-aggregator-name-news-aggregator
---
# Design an API for a News Aggregator

Get a news aggregator API design with a content ingestion strategy and endpoints for source and topic preferences, personalized feeds, and search.

Variables: news_aggregator_name

## Prompt

I am building a news aggregator called {{news_aggregator_name}} that will collect news from various sources and present them to the user in a personalized feed.

Your task is to design the API for the news aggregator.

**Instructions:**
1.  **Content Ingestion:** Describe how you would collect news from various sources (e.g., RSS feeds, news APIs).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   User customization of news sources and topics.
    *   A personalized news feed.
    *   Searching for articles.

**Output Format:**
Provide the output as a Markdown document. First, describe your content ingestion strategy. Then, describe the design of your API endpoints.
