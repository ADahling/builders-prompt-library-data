---
title: "Identify and Remove Unused Functions in a Codebase"
slug: identify-and-remove-unused-functions-in-a-codebase
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/identify-and-remove-unused-functions-in-a-codebase
---
# Identify and Remove Unused Functions in a Codebase

Eliminate dead code by identifying unused functions across a codebase and generating a safe shell script to remove them for better efficiency.

Variables: language, source_directory, exclude_patterns

## Prompt

You are an expert code reviewer. I need you to analyze my project's codebase, which is written in {{language}}. Your task is to identify all functions that are declared but never called, and are therefore considered "dead code." 

Please provide a list of these unused functions, including the file path and line number for each. For each function, explain why it is being flagged as unused (e.g., "not called anywhere in the project"). 

After listing the dead functions, generate a shell script that will automatically remove them from the codebase. The script should be safe to run and should not remove any code that might be used dynamically or through reflection if your analysis cannot account for that. 

Finally, provide a summary of the potential benefits of removing this dead code, such as improved code clarity, reduced maintenance overhead, and smaller bundle size.

Project details:
- Language: {{language}}
- Source code directory: {{source_directory}}
- Exclude patterns (optional): {{exclude_patterns}}

Output format:
1.  **List of Unused Functions:** A markdown table with columns for "File Path," "Line Number," "Function Name," and "Reason for Removal."
2.  **Removal Script:** A shell script to delete the identified functions.
3.  **Summary of Benefits:** A brief explanation of the advantages of this cleanup.

## Tips

A good first step for any code cleanup initiative. Be cautious with dynamically called functions.
