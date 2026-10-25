---
title: "Designing a Global Configuration Management System"
slug: designing-a-global-configuration-management-system
stage: Build
category: "System Architecture"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-global-configuration-management-system
---
# Designing a Global Configuration Management System

Design a highly available global configuration system using a central key-value store and local agents for low-latency dynamic updates.

## Prompt

You are a platform engineer at a company with services deployed across multiple regions. You need a centralized system for managing application configuration.

**Your Task:**
Design a global, highly available configuration management system.

**Instructions & Constraints:**
1.  **Requirements:**
    *   Centralized storage for configuration data.
    *   High availability.
    *   Low-latency access to configuration from applications.
    *   Ability to update configuration dynamically without restarting services.

2.  **Core Component: The Configuration Store:**
    *   Propose using a strongly consistent key-value store like etcd or ZooKeeper as the central source of truth for the configuration.

3.  **Architecture:**
    *   Design an architecture where applications do not talk directly to the central store. Instead, they talk to a local agent or cache.
    *   The local agent watches the central store for changes and updates a local cache.
    *   Applications read their configuration from the local cache.

4.  **Dynamic Updates:**
    *   Explain how this architecture enables dynamic updates. When a value is changed in the central store, the agents are notified, they update their local caches, and the applications can then reload the configuration.

**Output Format:**
Generate a design document in Markdown:
1.  **The Need for a Global Configuration Management System**
2.  **Our High-Level Architecture**
3.  **The Role of the Central Store and the Local Agent**
4.  **A System for Dynamic, Real-Time Configuration Updates**
