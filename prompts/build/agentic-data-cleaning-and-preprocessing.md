---
title: "Agentic Data Cleaning and Preprocessing"
slug: agentic-data-cleaning-and-preprocessing
stage: Build
category: "AI Agent Development"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-data-cleaning-and-preprocessing
---
# Agentic Data Cleaning and Preprocessing

Get a Python pandas agent demo that handles missing values, removes duplicates, corrects data types, and saves a cleaned CSV dataset.

Variables: file_path, output_path

## Prompt

Design an AI agent that can automate the process of cleaning and preprocessing a messy CSV dataset. The agent should be able to identify and handle common data quality issues.

**Agent's Capabilities:**

The agent should have tools to:
1.  Load a CSV file into a pandas DataFrame.
2.  Identify missing values (`.isnull().sum()`).
3.  Suggest and apply a strategy for handling missing values (e.g., fill with mean, median, or a constant).
4.  Detect and remove duplicate rows.
5.  Identify columns with incorrect data types (e.g., a number column stored as a string).
6.  Save the cleaned DataFrame to a new CSV file.

**Implementation:**

*   Use LangChain's `create_pandas_dataframe_agent`.
*   The agent will use an LLM to generate and execute pandas code to perform the cleaning steps.
*   **The Prompt:** Your prompt to the agent should be a high-level instruction, like: "Clean the provided dataset located at `{{file_path}}`. Handle missing values, remove duplicates, and correct data types. Save the cleaned data to `{{output_path}}`."

**Your Task:**

Create a Python script that initializes the pandas agent and runs it with a messy CSV file (you can create a small sample one for the demo). The script should show the agent's thought process as it decides which cleaning steps to apply.

**Output:**

A Python script that demonstrates the data cleaning agent, along with the contents of the final cleaned CSV file.
