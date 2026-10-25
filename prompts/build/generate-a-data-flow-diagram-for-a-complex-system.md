---
title: "Generate a Data Flow Diagram for a Complex System"
slug: generate-a-data-flow-diagram-for-a-complex-system
stage: Build
category: "Backend & Data Integrity"
grade: C
score: 69
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-data-flow-diagram-for-a-complex-system
---
# Generate a Data Flow Diagram for a Complex System

Get multilevel data flow diagrams, a data dictionary, explanatory narrative, and tool recommendations for a system security audit.

Variables: system_name

## Prompt

I need to document the flow of data through our {{system_name}} system for a security audit. The system is complex, with multiple microservices, databases, and third-party integrations. I need a clear and accurate data flow diagram (DFD) that shows how data is created, processed, stored, and transmitted.

Your task is to generate a comprehensive data flow diagram and accompanying documentation. This should include:

1.  **DFD Levels:** A set of DFDs at different levels of abstraction, starting with a context diagram (Level 0) that shows the system as a single process, and then breaking it down into more detailed diagrams (Level 1, Level 2, etc.) for each major component.
2.  **DFD Components:** A clear and consistent use of DFD notation, including external entities, processes, data stores, and data flows.
3.  **Data Dictionary:** A data dictionary that describes each data flow and data store in detail. For each data element, it should specify its name, type, format, and any validation rules.
4.  **Narrative:** A narrative that walks through the DFDs and explains the flow of data in plain English. This should highlight the key data processing steps and the interactions between the different components.
5.  **Tool Recommendation:** A recommendation for a tool to create and maintain the DFDs (e.g., Lucidchart, draw.io, or a specialized DFD tool).

## Tips

This prompt helps in creating a clear and understandable representation of a complex system's data flows, which is essential for security, compliance, and onboarding new team members.
