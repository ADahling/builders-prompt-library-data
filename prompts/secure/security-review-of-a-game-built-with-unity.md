---
title: "Security Review of a Game Built with Unity"
slug: security-review-of-a-game-built-with-unity
stage: Secure
category: "Security Review"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-review-of-a-game-built-with-unity
---
# Security Review of a Game Built with Unity

Conduct a comprehensive security audit of a Unity mobile game to identify vulnerabilities in client-side code, server APIs, and payment systems.

Variables: game_name

## Prompt

You are a security engineer reviewing a new mobile game, {{game_name}}, built with the Unity game engine. The game includes in-app purchases and a server-side component for managing player data. Your goal is to identify and mitigate security vulnerabilities in the game.

Create a detailed security review report in Markdown. The report should cover the following areas:

1.  **Client-Side Security:**
    *   Is the game vulnerable to cheating (e.g., memory editing, speed hacking)?
    *   Are there any anti-cheat mechanisms in place?
    *   How are game assets protected from tampering?

2.  **Server-Side Security:**
    *   How does the game client communicate with the server?
    *   Is the server vulnerable to common web vulnerabilities (e.g., SQL injection, XSS)?
    *   How is player data protected on the server?

3.  **In-App Purchase Security:**
    *   How are in-app purchases handled?
    *   Is the game vulnerable to purchase fraud?

4.  **Third-Party SDKs:**
    *   Does the game use any third-party SDKs (e.g., for analytics, ads)?
    *   Are these SDKs secure?

For each area, provide your assessment and a list of prioritized recommendations for improvement. Your report should be a practical guide for the game development team to improve the security of the game.
