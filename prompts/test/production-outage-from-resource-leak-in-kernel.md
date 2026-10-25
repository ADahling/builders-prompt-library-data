---
title: "Production Outage from Resource Leak in Kernel"
slug: production-outage-from-resource-leak-in-kernel
stage: Test
category: "Critical Bugs"
grade: C
score: 67
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-from-resource-leak-in-kernel
---
# Production Outage from Resource Leak in Kernel

Identify and resolve kernel-level resource leaks using debugging tools like kmemleak and eBPF while implementing robust error-handling patterns.

## Prompt

You are a kernel developer. A production server has been crashing after running for a few weeks. The crash is a kernel panic, and the logs indicate that the kernel has run out of a specific resource, like a particular type of memory pool or file descriptors. You suspect a resource leak in a custom kernel module. Your task is to find and fix the leak.

Context:
- The server is running Linux with a custom kernel module for a high-performance networking device.
- The module allocates a resource when the device is opened but does not always free it when the device is closed, especially in error paths.
- You have access to kernel debugging tools.

Provide:
1. A guide on how to use kernel debugging tools like `kmemleak` or custom tracing with `ftrace` or `eBPF` to track the allocation and deallocation of the specific resource and identify the code path that is leaking.
2. An example of a common resource leak pattern in a kernel module (e.g., failing to release a resource in an error handling path after a `goto`).
3. The corrected code that ensures the resource is always freed in all code paths, using the standard `goto` cleanup pattern common in C and kernel code.

## Tips

An extremely challenging problem that requires deep expertise in kernel development and debugging.
