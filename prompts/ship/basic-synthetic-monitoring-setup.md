---
title: "Basic Synthetic Monitoring Setup"
slug: basic-synthetic-monitoring-setup
stage: Ship
category: "Monitoring & Observability"
grade: B
score: 75
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/basic-synthetic-monitoring-setup
---
# Basic Synthetic Monitoring Setup

Configure automated synthetic checks to monitor critical web performance metrics and user journeys with periodic testing and email alerts.

Variables: monitoring_tool, website_url

## Prompt

You are tasked with setting up basic synthetic monitoring for a web application. Use the {{monitoring_tool}} to simulate user interactions on the homepage of {{website_url}}. Your goal is to ensure that all critical interactions such as page load, button clicks, and form submissions are functioning correctly. Define a testing schedule that runs these checks every 15 minutes. Provide an example configuration file for these checks. Ensure that your setup includes alerting via email when a check fails. Document the steps taken to implement this solution and any challenges encountered.

## Tips

This prompt is aimed at developers new to synthetic monitoring, focusing on basic setup and configuration.
