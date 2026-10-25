---
title: "System Design Interview: Design a Hotel Booking System"
slug: system-design-interview-design-a-hotel-booking-system
stage: Build
category: "System Architecture"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/system-design-interview-design-a-hotel-booking-system
---
# System Design Interview: Design a Hotel Booking System

Architect a scalable hotel booking system that prevents double-bookings through robust concurrency controls and distributed microservices.

## Prompt

You are in a system design interview. The interviewer asks you to "Design a hotel booking system like Booking.com or Expedia."

**Your Task:**
Provide a high-level design for a hotel booking system.

**Instructions & Constraints:**
1.  **Requirements:**
    *   Users can search for hotels.
    *   Users can book rooms.
    *   The system must handle concurrency correctly (i.e., don't double-book a room).

2.  **Architecture:**
    *   **Search Service:** A service for searching for hotels.
    *   **Booking Service:** A service for managing bookings.
    *   **Inventory Service:** A service that manages the hotel room inventory.

3.  **Handling Concurrency:**
    *   This is the key challenge. Discuss how to prevent two users from booking the same room at the same time. This will involve using database transactions and locking.

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Hotel Booking System**
2.  **High-Level Architecture**
3.  **The Critical Challenge: Handling Concurrent Bookings**
