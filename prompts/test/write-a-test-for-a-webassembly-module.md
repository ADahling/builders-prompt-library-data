---
title: "Write a Test for a WebAssembly Module"
slug: write-a-test-for-a-webassembly-module
stage: Test
category: "Testing & QA"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-test-for-a-webassembly-module
---
# Write a Test for a WebAssembly Module

Generate functional unit tests and performance benchmarks for WebAssembly modules to ensure cross-runtime reliability and execution speed.

Variables: programming_language, module_purpose

## Prompt

You are a systems programmer. Your task is to write a test for a WebAssembly (Wasm) module to verify its correctness and performance. The Wasm module is written in {{programming_language}} and it {{module_purpose}}.

Context:
- You need to test the Wasm module in a browser environment and in a standalone Wasm runtime.
- You will write tests for the functions exported by the Wasm module.

Provide:
1. A test that loads the Wasm module and calls its exported functions with some sample data.
2. Assertions to verify that the functions return the correct results.
3. A benchmark to measure the performance of the Wasm module.

## Tips

An advanced prompt for programmers who are working with WebAssembly and want to learn how to test their modules.
