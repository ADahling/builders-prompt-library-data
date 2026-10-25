---
title: "Develop a LangChain Agent with Custom Tools for GitHub Repository Analysis"
slug: develop-a-langchain-agent-with-custom-tools-for-github-repository-analysis
stage: Build
category: "AI Agent Development"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/develop-a-langchain-agent-with-custom-tools-for-github-repository-analysis
---
# Develop a LangChain Agent with Custom Tools for GitHub Repository Analysis

Architect a ReAct-based LangChain agent that clones GitHub repositories and uses custom tools to generate structured technical summaries.

Variables: owner, repo_name

## Prompt

You are an expert AI developer specializing in LangChain. Your task is to create a Python script that builds an AI agent capable of analyzing a GitHub repository. The agent must use a set of custom-defined tools to perform its analysis.

**Project Requirements:**

1.  **Agent Type:** Use the ReAct (Reasoning and Acting) framework for the agent.
2.  **LLM:** Use the `ChatOpenAI` model with `gpt-5`.
3.  **Custom Tools:** Implement the following custom tools using LangChain's `Tool` class:
    *   `list_files`: Lists all files in the root of the repository.
    *   `read_file`: Reads the content of a specific file.
    *   `get_repo_structure`: Returns a tree-like structure of the repository's directories and files.
4.  **Input:** The agent should accept a GitHub repository URL as input (e.g., 'https://github.com/{{owner}}/{{repo_name}}').
5.  **Process:** The agent should first clone the repository to a local directory. Then, it should use the custom tools to understand the repository's structure and content. Finally, it should provide a summary of the repository, including:
    *   The primary programming language used.
    *   Key libraries or frameworks identified.
    *   A brief description of the project's purpose based on the README file and source code.

**Constraints:**

*   The script must be well-documented with comments explaining each major step.
*   Error handling should be implemented for tool execution (e.g., file not found).
*   The final output should be a JSON object containing the analysis summary.

**Example Output Format:**

'''json
{
  "repository": "{{owner}}/{{repo_name}}",
  "language": "Python",
  "frameworks": ["LangChain", "FastAPI"],
  "summary": "This project is a conversational AI agent that uses LangChain to interact with a custom API..."
}
'''
