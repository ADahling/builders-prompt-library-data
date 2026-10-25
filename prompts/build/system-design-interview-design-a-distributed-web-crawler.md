---
title: "System Design Interview: Design a Distributed Web Crawler"
slug: system-design-interview-design-a-distributed-web-crawler
stage: Build
category: "System Architecture"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-design-interview-design-a-distributed-web-crawler
---
# System Design Interview: Design a Distributed Web Crawler

Architect a high-scale, distributed web crawler featuring URL frontier management, politeness protocols, and duplicate detection systems.

## Prompt

You are in a system design interview. The interviewer asks you to "Design a distributed web crawler."

**Your Task:**
Provide a detailed design for a distributed web crawler that can crawl the entire web.

**Instructions & Constraints:**
1.  **Challenges of Web-Scale Crawling:**
    *   Discuss the challenges: massive scale, politeness, duplicate content.

2.  **Distributed Architecture:**
    *   Design a distributed architecture with multiple crawler nodes.
    *   **URL Frontier:** A distributed queue to manage the URLs to be crawled.
    *   **Fetcher and Parser Nodes:** A fleet of nodes to download and parse pages.
    *   **Duplicate Detection:** A system to detect duplicate content (e.g., using shingles and a distributed hash table).

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Web-Scale Distributed Crawler**
2.  **A Distributed Architecture for Crawling the Web**
3.  **Managing the Frontier and Ensuring Politeness**
4.  **Handling Duplicate Content at Scale**
