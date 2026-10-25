---
title: "Basic Kubernetes Pod Status Check"
slug: basic-kubernetes-pod-status-check
stage: Ship
category: "Monitoring & Observability"
grade: C
score: 61
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/basic-kubernetes-pod-status-check
---
# Basic Kubernetes Pod Status Check

Audit Kubernetes pod statuses within a specific namespace to identify errors and receive actionable troubleshooting recommendations.

Variables: project_name, namespace_name, pod_name, status, error_messages, recommendations

## Prompt

You are tasked with monitoring the status of Kubernetes pods in the cluster for the {{project_name}} project. Your goal is to ensure that all pods are running smoothly without any errors. Use the Kubernetes CLI to fetch the current status of all pods in the namespace {{namespace_name}}. Once you have gathered the information, summarize the status of each pod, including their names, current states, and any error messages if they exist. Provide recommendations for addressing any issues found. Your output should be structured as follows:

1. Pod Name: {{pod_name}}
   - Status: {{status}}
   - Error Messages: {{error_messages}}
2. Overall Recommendations: {{recommendations}}

Ensure that all information is accurate and up-to-date, reflecting the current state of the cluster.

## Tips

This prompt helps beginners understand how to check the status of Kubernetes pods.
