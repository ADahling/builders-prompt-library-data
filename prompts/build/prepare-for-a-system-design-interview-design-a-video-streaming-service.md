---
title: "Prepare for a System Design Interview: Design a Video Streaming Service"
slug: prepare-for-a-system-design-interview-design-a-video-streaming-service
stage: Build
category: "System Architecture"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/prepare-for-a-system-design-interview-design-a-video-streaming-service
---
# Prepare for a System Design Interview: Design a Video Streaming Service

Architect a scalable video streaming platform by defining ingestion pipelines, transcoding workflows, and CDN-driven playback strategies.

## Prompt

You are a principal engineer in a system design interview. The prompt is: "Design a video streaming service like YouTube or Netflix."

**Your Task:**
Provide a comprehensive, end-to-end design that covers everything from video ingestion to playback. This is a complex problem, so you need to demonstrate a deep understanding of various infrastructure components.

**Instructions & Constraints:**
Structure your response as follows:

1.  **Requirements and Goals:**
    *   **Functional:** Users can upload videos. Videos should be available for playback on various devices (web, mobile) and at different quality levels. Users can search for videos.
    *   **Non-Functional:** High availability and durability of videos. Low latency for video playback (fast start time). Scalability to serve millions of concurrent viewers.

2.  **High-Level End-to-End Design:**
    *   Draw a high-level diagram that shows the two main workflows: the **video ingestion workflow** and the **video playback workflow**.

3.  **Deep Dive: Video Ingestion Workflow:**
    *   This is the process that happens after a user uploads a video.
    *   **Upload:** The video is uploaded to a web server.
    *   **Transcoding:** This is a crucial step. Explain that the original video needs to be converted into multiple formats and resolutions (e.g., 1080p, 720p, 480p) to support different devices and network conditions. This is a CPU-intensive process that should be done by a fleet of dedicated worker servers.
    *   **Adaptive Bitrate Streaming:** Explain that the video is broken down into small chunks (e.g., a few seconds long). This allows the video player to switch between quality levels seamlessly based on the user's network speed.
    *   **Storage:** The transcoded video chunks are stored in a highly durable and scalable object store (like Amazon S3 or Google Cloud Storage).
    *   **Metadata:** The metadata about the video (title, description, chunk locations) is stored in a database.

4.  **Deep Dive: Video Playback Workflow:**
    *   This is what happens when a user clicks "play".
    *   **Client Request:** The client (e.g., a web browser) requests the video.
    *   **Content Delivery Network (CDN):** This is the most important component for a scalable streaming service. Explain that the video chunks are not served directly from the object store. Instead, they are cached at CDN edge locations all over the world, close to the users.
    *   **Playback:** The video player on the client device downloads the video chunks and plays them. It uses a manifest file (also delivered via the CDN) to know which chunks to download and at which quality.

5.  **Database and Search:**
    *   Discuss the database schema for video metadata.
    *   Explain how you would implement the search functionality (e.g., using a dedicated search index like Elasticsearch).

6.  **Scaling and Cost:**
    *   Discuss how the CDN is the key to scaling the read-heavy playback workflow.
    *   Talk about the cost implications, especially the bandwidth costs from the CDN.

**Output Format:**
Generate a detailed Markdown document that clearly explains your end-to-end design.
