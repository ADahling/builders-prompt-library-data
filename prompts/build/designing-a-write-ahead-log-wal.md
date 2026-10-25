---
title: "Designing a Write-Ahead Log (WAL)"
slug: designing-a-write-ahead-log-wal
stage: Build
category: "System Architecture"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-write-ahead-log-wal
---
# Designing a Write-Ahead Log (WAL)

Architect a robust Write-Ahead Log system featuring record schemas, commit protocols, and crash recovery mechanisms to ensure data durability.

## Prompt

You are a database engineer designing a new storage engine. A critical component for ensuring data durability and enabling crash recovery is the Write-Ahead Log (WAL). 

**Your Task:**
Design the Write-Ahead Log for your storage engine. The design should be detailed and cover the format of the log, the process of writing to it, and how it's used for crash recovery.

**Instructions & Constraints:**
1.  **The Purpose of a WAL:**
    *   Explain the principle of write-ahead logging: before any change is made to the actual data files on disk, a record of that change must first be written to a separate, append-only log file.
    *   Describe the two main benefits of this approach: **durability** (once the log record is flushed to disk, the change is considered durable) and **performance** (it turns many small, random writes into a single sequential write to the log).

2.  **Log Record Format:**
    *   Design the format of a single record in your WAL. It should contain information like:
        *   A unique log sequence number (LSN).
        *   The transaction ID.
        *   The type of operation (e.g., INSERT, UPDATE, DELETE).
        *   The location of the data being changed (e.g., table ID, page ID, row ID).
        *   The "before" and "after" images of the data (for undo and redo).

3.  **The Writing Process:**
    *   Describe the process that occurs when a transaction modifies data:
        1.  A log record is created in memory.
        2.  The log record is appended to the WAL buffer in memory.
        3.  At transaction commit time, the WAL buffer (up to the commit record) is flushed to the log file on disk.
        4.  Only after the log is safely on disk can the transaction be acknowledged as committed.
        5.  The actual data pages (the "dirty pages") can be written to disk later in the background.

4.  **Crash Recovery:**
    *   This is the key use of the WAL. Describe the recovery process after a crash:
        1.  The database starts up and finds the last checkpoint.
        2.  It then replays the WAL from the last checkpoint forward.
        3.  It uses the "after" images in the log records to **redo** any changes from committed transactions that were not yet written to the data files.
        4.  It uses the "before" images to **undo** any changes from uncommitted (rolled back) transactions that were written to the data files.

5.  **Checkpoints and Log Truncation:**
    *   Explain the role of checkpoints. A checkpoint is a point in time where all dirty pages have been flushed to disk. This allows the WAL to be truncated, preventing it from growing indefinitely.

**Output Format:**
Create a detailed design document in Markdown:
1.  **The Write-Ahead Log: The Foundation of Durability**
2.  **Our WAL Record Format**
3.  **The Life of a Write: How We Use the WAL**
4.  **Surviving Crashes: The Recovery Process**
5.  **Checkpoints: Keeping the Log in Check**
