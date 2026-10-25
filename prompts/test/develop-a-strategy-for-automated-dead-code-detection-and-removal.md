---
title: "Develop a Strategy for Automated Dead Code Detection and Removal"
slug: develop-a-strategy-for-automated-dead-code-detection-and-removal
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/develop-a-strategy-for-automated-dead-code-detection-and-removal
---
# Develop a Strategy for Automated Dead Code Detection and Removal

Get a dead code removal strategy for your CI/CD pipeline with tool comparisons, dynamic usage safeguards, sample configuration, and approval steps.

Variables: tech_stack, language, ci_cd_platform

## Prompt

I want to implement an automated dead code detection and removal process for my {{tech_stack}} project. The goal is to create a robust and reliable CI/CD pipeline step that identifies and removes unused code without manual intervention. 

Your task is to devise a comprehensive strategy for this. Please consider the following aspects:

1.  **Tooling:** Recommend the best static analysis tools for {{language}} to identify dead code. Compare at least two tools, discussing their pros, cons, and configuration for this specific task.
2.  **Dynamic Usage:** How can we handle functions or modules that are used dynamically (e.g., through reflection, dependency injection frameworks, or string-based calls)? Propose a strategy to avoid false positives and the accidental removal of necessary code.
3.  **CI/CD Integration:** Describe how to integrate this process into a {{ci_cd_platform}} pipeline. Provide a sample configuration file (e.g., a GitHub Actions workflow YAML) that runs the analysis on every pull request and reports the findings.
4.  **Reporting and Approval:** How should the results be presented to the development team? Should the removal be fully automatic, or should there be a manual approval step? Suggest a workflow for this.

Output should be a detailed report covering these four points, with code snippets and configuration examples where applicable.

## Tips

This prompt moves beyond a one-time cleanup to establishing a sustainable process.
