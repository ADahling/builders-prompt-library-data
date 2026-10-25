---
title: "Reverse Engineering a Mobile App"
slug: reverse-engineering-a-mobile-app
stage: Secure
category: "Security Checklist"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/reverse-engineering-a-mobile-app
---
# Reverse Engineering a Mobile App

Decompile an Android APK using security tools to detect vulnerabilities like plaintext passwords or insecure local storage in the source code.

Variables: app_name

## Prompt

You are a mobile security researcher who wants to analyze the security of a popular Android application. You suspect that the app is storing sensitive data insecurely on the device. Your task is to reverse engineer the app to find out how it stores data.

Context:
- The app is `{{app_name}}`.
- You have the APK file for the app.

Provide:
1. A list of the tools you would use to reverse engineer the Android app (e.g., `apktool`, `dex2jar`, `jd-gui`).
2. A step-by-step guide on how to decompile the APK and analyze its source code.
3. A description of what you would look for in the code to identify insecure data storage practices (e.g., storing passwords in plaintext in SharedPreferences or a local database).

## Tips

A highly advanced prompt for those interested in mobile security and reverse engineering.
