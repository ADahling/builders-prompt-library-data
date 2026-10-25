---
title: "Kubernetes Pod Crash Troubleshooting"
slug: kubernetes-pod-crash-troubleshooting
stage: Build
category: "DevOps & IaC"
grade: A
score: 82
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/kubernetes-pod-crash-troubleshooting
---
# Kubernetes Pod Crash Troubleshooting

Get a pod crash diagnosis from kubectl output, with steps to verify the root cause and a suggested fix with example YAML changes.

## Prompt

Here's the output of kubectl describe pod my-app-pod: [paste output]. Analyze it and provide a step-by-step troubleshooting guide to identify the root cause (e.g., resource limits, config errors). Suggest a fix with example YAML changes. Format your response as: 1) Root Cause, 2) Steps to Verify, 3) Fix.

## Tips

The structured format (Root Cause → Verify → Fix) prevents the common mistake of jumping to solutions. Source: medium.com/@onix_react/ultimate-prompts-for-every-developer
