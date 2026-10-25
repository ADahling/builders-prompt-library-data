---
title: "Building a Simple 'Hello, World' Agent with LangChain"
slug: building-a-simple-hello-world-agent-with-langchain
stage: Build
category: "AI Agent Development"
grade: A+
score: 95
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-hello-world-agent-with-langchain
---
# Building a Simple 'Hello, World' Agent with LangChain

Get a Python greeting script with LangChain LCEL, ChatOpenAI, and API key setup to help beginners verify their environment.

Variables: name

## Prompt

Create the most basic "Hello, World" example of an AI agent using LangChain. This should be a complete, runnable script that a beginner can use to verify their setup.

**The Goal:**

Create an agent that, when given a user's name, says hello to them.

**The Components:**

1.  **LLM:** Use `ChatOpenAI`.
2.  **Prompt:** A `ChatPromptTemplate` that takes a `{{name}}` as input and has a template like: "Say hello to {{name}}."
3.  **Chain:** A simple `LLMChain` that pipes the prompt to the model.
4.  **Output Parser:** A `StrOutputParser` to get the final string output.

**Implementation (using LCEL):**

```python
from langchain_openai import ChatOpenAI
from langchain_core.prompts import ChatPromptTemplate
from langchain_core.output_parsers import StrOutputParser

# 1. LLM
model = ChatOpenAI()

# 2. Prompt
prompt = ChatPromptTemplate.from_template("Say hello to {{name}}")

# 3. Output Parser
parser = StrOutputParser()

# 4. Chain
chain = prompt | model | parser

# 5. Run
result = chain.invoke({"name": "World"})
print(result)
```

**Your Task:**

Provide a complete Python script that includes the necessary imports, environment variable setup (for the API key), and the LCEL chain shown above. The script should be ready to run out of the box.

**Output:**

A single, complete Python script.
