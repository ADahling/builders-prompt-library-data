---
title: "Find and Clean Up Unused Images and Media Assets"
slug: find-and-clean-up-unused-images-and-media-assets
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/find-and-clean-up-unused-images-and-media-assets
---
# Find and Clean Up Unused Images and Media Assets

Get a guide to finding unused website media assets with a tool or script, including setup, analysis commands, and checks before deletion.

Variables: assets_directory

## Prompt

My project's asset directory (`{{assets_directory}}`) is full of images, videos, and other media files. I'm sure many of them are no longer used on the website, but finding them manually is tedious.

Your task is to provide a simple way to find and remove these unused assets.

1.  **The Problem:** Explain why unused assets are a problem (e.g., bloated repository size, longer build times, confusion for developers).
2.  **Tool Recommendation:** Recommend a command-line tool or script that can scan the codebase (HTML, CSS, JavaScript files) to see which assets are referenced, and then compare that to the list of files in the assets directory.
3.  **Step-by-Step Guide:** Provide a step-by-step guide on how to use the recommended tool. Include:
    *   Installation command.
    *   The command to run the analysis.
    *   How to interpret the output (the list of unused files).
4.  **Safety Precautions:** What precautions should I take before deleting the files? (e.g., make sure the tool can detect dynamically generated asset paths, double-check the list before deleting, make sure the project is under version control).

Output should be a simple, practical guide for a quick cleanup win.

## Tips

A straightforward cleanup task that can reduce the size of your project repository.
