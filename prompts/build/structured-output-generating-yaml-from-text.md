---
title: "Structured Output: Generating YAML from Text"
slug: structured-output-generating-yaml-from-text
stage: Build
category: "LLM & AI Integration"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-generating-yaml-from-text
---
# Structured Output: Generating YAML from Text

Convert natural language requirements into valid, raw GitHub Actions YAML configurations for automated CI/CD workflow generation.

## Prompt

As a DevOps engineer, you often work with YAML files for configuration (e.g., Kubernetes, GitHub Actions). You want to use an LLM to automatically generate a YAML configuration file based on a natural language description of the desired setup.

Your task is to create a prompt for an LLM that can reliably convert a description into a valid YAML file.

**Scenario:**
- **User Request:** "I need a GitHub Actions workflow that runs when I push to the main branch. It should have one job called 'build' that runs on ubuntu-latest. The job should have two steps: first, check out the code, and second, run 'npm install'."
- **Desired YAML Output:**
`name: CI
on:
  push:
    branches:
      - main
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Check out code
        uses: actions/checkout@v3
      - name: Install dependencies
        run: npm install`

**Prompt Engineering Task:**
You are not writing code, but the prompt itself.

**Prompt Requirements:**
1.  **Role Definition:** "You are an expert DevOps engineer specializing in CI/CD and GitHub Actions."
2.  **The Task:** "Your task is to convert the following natural language request into a valid GitHub Actions workflow YAML file."
3.  **Input Data:** Provide the user's request.
4.  **Constraints:** "The output must be a single block of valid YAML. Do not include any extra text, explanations, or markdown code fences (like `yaml`). The output should be the raw YAML content itself, starting with the 'name' key."

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the LLM.
