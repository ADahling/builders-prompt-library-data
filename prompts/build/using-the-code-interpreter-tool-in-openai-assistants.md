---
title: "Using the Code Interpreter Tool in OpenAI Assistants"
slug: using-the-code-interpreter-tool-in-openai-assistants
stage: Build
category: "AI Agent Development"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/using-the-code-interpreter-tool-in-openai-assistants
---
# Using the Code Interpreter Tool in OpenAI Assistants

Build a Python script using OpenAI Assistants Code Interpreter to upload sales CSV data, analyze regional totals, and download a bar chart.

Variables: sales_data.csv

## Prompt

Demonstrate how to use the Code Interpreter tool within OpenAI's Assistants API to perform data analysis on an uploaded file.

**Scenario:**

You have a CSV file containing sales data (`{{sales_data.csv}}`). You want the assistant to analyze this data and create a visualization.

**Implementation Steps:**

1.  **Upload the File:** Use the OpenAI API to upload the CSV file. You will get a file ID in return.
2.  **Create the Assistant:** Create an assistant and enable the `code_interpreter` tool.
3.  **Create a Thread and Attach the File:** Create a new thread. When adding the user's message to the thread, attach the file ID you obtained in step 1.
    *   User Message: "Analyze the attached sales data. Calculate the total sales per region and generate a bar chart showing the results."
4.  **Run the Assistant:** Initiate a run on the thread.
5.  **Retrieve the Results:**
    *   Poll the run status.
    *   Once completed, retrieve the messages.
    *   The assistant's response should include the text analysis and a file ID for the generated chart image.
6.  **Download the Image:** Write the code to download the generated image file using the OpenAI API and save it locally.

**Output:**

A complete Python script that executes this entire workflow, from uploading the data to downloading the final chart.
