---
title: "Fix a Memory Leak from Unclosed File Handles"
slug: fix-a-memory-leak-from-unclosed-file-handles
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-memory-leak-from-unclosed-file-handles
---
# Fix a Memory Leak from Unclosed File Handles

Identify and resolve Python memory leaks by replacing unclosed file handles with context managers to ensure efficient resource management.

## Prompt

You are a Python developer. You have written a script that processes thousands of files. You notice that the script’s memory usage grows over time and it eventually crashes. You realize that you are opening files but not closing them.

Context:
- The script loops through a directory of files and opens each one for reading.
- The operating system has a limit on the number of open file handles a process can have.
- Each open file handle consumes a small amount of memory in the kernel.

Provide:
1. A Python code snippet that demonstrates the problem by opening files in a loop without closing them.
2. An explanation of why it is important to close file handles and what happens if you don’t.
3. The corrected Python code that uses the `with open(...) as f:` syntax, which automatically closes the file handle, even if errors occur inside the `with` block.

## Tips

A fundamental best practice for I/O operations in any programming language.
