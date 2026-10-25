---
title: "Manage Configuration Drift Between Environments"
slug: manage-configuration-drift-between-environments
stage: Ship
category: "Deployment & Launch"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/manage-configuration-drift-between-environments
---
# Manage Configuration Drift Between Environments

Align environment configurations using IaC and automated management tools to eliminate production-only bugs caused by infrastructure drift.

Variables: iac_tool, config_management_tool

## Prompt

You are an SRE. You have noticed that the configuration of your staging and production environments has drifted over time, causing issues that only appear in production. Your task is to manage this drift.

Instructions:
1. Use Infrastructure as Code (`{{iac_tool}}`) to define your environments declaratively.
2. Use a configuration management tool (`{{config_management_tool}}`) to enforce the state of your servers.
3. Implement a process for regularly comparing the configuration of your environments.
4. The goal is to make your environments as identical as possible, except for a few well-defined differences.

## Tips

A common problem that can be solved with the right tools and processes.
