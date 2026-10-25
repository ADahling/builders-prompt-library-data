---
title: "Generate API Documentation from Source Code Comments"
slug: generate-api-documentation-from-source-code-comments
stage: Design
category: "Documentation"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-api-documentation-from-source-code-comments
---
# Generate API Documentation from Source Code Comments

Automate the creation of HTML API documentation by generating a script that installs a chosen tool and parses source code comments.

Variables: language, documentation_tool, source_code_directory, output_directory

## Prompt

You are a software developer working on a {{language}} project. To streamline the process of creating API documentation, you want to generate it automatically from comments in your source code using {{documentation_tool}}.

Your task is to write a script that will scan your source code, extract the documentation comments, and generate a set of HTML documentation files. The script should:

1.  Install {{documentation_tool}} if it is not already installed.
2.  Define the source code directory to be scanned.
3.  Specify the output directory for the generated documentation.
4.  Run the {{documentation_tool}} command with the appropriate options to generate the documentation.

Here is some information about your project:

*   **Language:** {{language}}
*   **Source Code Directory:** {{source_code_directory}}
*   **Output Directory:** {{output_directory}}

Generate the complete script. The script should be well-commented and easy to run.
