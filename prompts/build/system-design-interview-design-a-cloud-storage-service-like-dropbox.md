---
title: "System Design Interview: Design a Cloud Storage Service like Dropbox"
slug: system-design-interview-design-a-cloud-storage-service-like-dropbox
stage: Build
category: "System Architecture"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-design-interview-design-a-cloud-storage-service-like-dropbox
---
# System Design Interview: Design a Cloud Storage Service like Dropbox

Draft a high-level system architecture and synchronization protocol for a scalable cloud storage service to prepare for technical interviews.

## Prompt

You are in a system design interview. The interviewer asks you to "Design a cloud storage service like Dropbox or Google Drive."

**Your Task:**
Provide a high-level design for a cloud storage service.

**Instructions & Constraints:**
1.  **Core Features:**
    *   Users can upload and download files.
    *   Files are synced across multiple devices.

2.  **Architecture:**
    *   **Client Application:** A client that runs on the user's device.
    *   **Metadata Store:** A database to store the metadata about files and users.
    *   **Block Store:** A scalable object store (like S3) to store the actual file data.
    *   **Synchronization Service:** A service to manage the synchronization of files.

3.  **File Synchronization:**
    *   Discuss how the client would detect changes and sync them with the server.

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Cloud Storage and Synchronization Service**
2.  **High-Level Architecture**
3.  **The File Synchronization Protocol**
