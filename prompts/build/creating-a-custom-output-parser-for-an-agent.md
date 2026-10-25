---
title: "Creating a Custom Output Parser for an Agent"
slug: creating-a-custom-output-parser-for-an-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-custom-output-parser-for-an-agent
---
# Creating a Custom Output Parser for an Agent

Get a Python example using a Pydantic schema, output parser, and LangChain LCEL chain for agent integrations that need structured data.

## Prompt

Develop a custom output parser for a LangChain agent to ensure it always returns its final answer in a specific JSON format. This is crucial when integrating agents into larger software systems that expect structured data.

**The Problem:**

By default, agents often return plain text. If you need the agent to extract specific fields (e.g., a name, a date, and a summary), parsing plain text is unreliable.

**Your Task:**

1.  **Define the Schema:** Use Pydantic to define the expected output structure. For example:
    ```python
    class AgentResponse(BaseModel):
        action_taken: str = Field(description="A brief description of what the agent did.")
        final_answer: str = Field(description="The actual answer to the user's query.")
        confidence_score: int = Field(description="A score from 1-10 indicating confidence.")
    ```
2.  **Create the Parser:** Instantiate a `PydanticOutputParser` with your schema.
3.  **Modify the Prompt:** Inject the parser's format instructions into the agent's prompt. This tells the LLM *how* to format its output.
4.  **Build the Chain:** Create an LCEL chain that combines the prompt, the LLM, and your custom parser.

**Example Usage:**

*   User: "What is the capital of France and how confident are you?"
*   The chain should return a parsed Pydantic object (or a dictionary), not a string.

**Output:**

A Python script demonstrating the definition of the Pydantic schema, the setup of the parser, and the execution of the chain returning structured JSON.
