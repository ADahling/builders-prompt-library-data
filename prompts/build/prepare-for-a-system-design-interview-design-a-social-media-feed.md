---
title: "Prepare for a System Design Interview: Design a Social Media Feed"
slug: prepare-for-a-system-design-interview-design-a-social-media-feed
stage: Build
category: "System Architecture"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/prepare-for-a-system-design-interview-design-a-social-media-feed
---
# Prepare for a System Design Interview: Design a Social Media Feed

Construct a comprehensive architectural blueprint for a scalable, high-availability social media news feed using hybrid push/pull delivery strategies.

## Prompt

You are a senior software engineer in a system design interview. The prompt is: "Design the news feed of a social media application like Twitter or Facebook."

**Your Task:**
Provide a detailed, structured response that covers all the key aspects of designing a large-scale social media feed. Your goal is to demonstrate your ability to handle complex, read-heavy systems.

**Instructions & Constraints:**
Follow this structured approach:

1.  **Functional and Non-Functional Requirements:**
    *   **Functional:** Users can post content (text, images). Users can follow other users. The feed should show posts from followed users in reverse chronological order.
    *   **Non-Functional:** The system must be highly available and scalable. Generating the feed should be fast (e.g., under 200ms). The system should be eventually consistent.

2.  **Capacity Estimation:**
    *   Assume some numbers (e.g., 500 million daily active users, each user follows 100 others, each user posts once per day). 
    *   Estimate the read/write ratio (it will be heavily read-biased).
    *   Estimate the storage requirements for posts and the social graph.

3.  **High-Level Design:**
    *   Draw a diagram showing the main services: User Service, Post Service, Follow Service, and a News Feed Generation Service.
    *   Describe the APIs for these services.

4.  **Feed Generation Approaches (The Core of the Problem):**
    *   This is the most important part. Compare two main approaches:
        *   **Pull-Based (On-the-fly Generation):**
            *   Explain how it works: When a user requests their feed, the system fetches the IDs of all the people they follow, gets the latest posts from each of them, and merges them.
            *   Discuss the pros (simple, no extra storage) and cons (slow for users who follow many people, the "celebrity problem").
        *   **Push-Based (Pre-computed/Fan-out):**
            *   Explain how it works: When a user posts, the system immediately pushes this post into the feeds of all their followers. The feed is stored in a cache (like Redis).
            *   Discuss the pros (fast reads) and cons (high write load, especially for celebrities, wasted resources for inactive users).

5.  **A Hybrid Approach (The Recommended Solution):**
    *   Propose a hybrid approach that combines the best of both worlds.
    *   For most users, use the push-based approach.
    *   For "celebrities" (users with millions of followers), do not fan out their posts. Instead, when a user who follows a celebrity requests their feed, fetch the celebrity's posts on-the-fly and merge them with the pre-computed feed.

6.  **Database and Caching:**
    *   Discuss your choice of database for storing posts (e.g., a NoSQL database like Cassandra) and the social graph (e.g., a graph database or a simple SQL table).
    *   Explain how you would use a cache like Redis to store the pre-computed feeds (e.g., using Redis Lists or Sorted Sets).

7.  **Scaling and Further Optimizations:**
    *   Discuss sharding the user and post data.
    *   Talk about using a CDN for media content.

**Output Format:**
Generate a comprehensive Markdown document that presents your solution in a clear, interview-ready format.
