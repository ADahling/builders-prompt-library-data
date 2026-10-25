---
title: "Fix an Infinite Loop in a Game\u2019s Physics Engine"
slug: fix-an-infinite-loop-in-a-game-s-physics-engine
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-an-infinite-loop-in-a-game-s-physics-engine
---
# Fix an Infinite Loop in a Game’s Physics Engine

Debug and resolve persistent collision jitter in a 2D physics engine by implementing a robust minimum translation vector algorithm.

## Prompt

You are a game developer. You are working on a 2D platformer game. You have a bug where the player character sometimes gets stuck inside a wall and jitters violently. You realize this is an infinite loop in your collision resolution code.

Context:
- The game loop updates the player’s position, then checks for collisions with the level geometry.
- If a collision is detected, the code tries to move the player out of the wall.
- However, the resolution logic is flawed, and it sometimes moves the player to a new position that is also inside the wall, or even pushes them further in. The next frame, it detects a collision again and tries to resolve it again, leading to an infinite loop of small, opposing movements.

Provide:
1. A description of a simple but flawed collision resolution algorithm that could cause this problem.
2. An explanation of why the character gets stuck and jitters (it’s being pushed back and forth across the wall boundary). 
3. A more robust collision resolution algorithm. A common approach is to calculate the minimum translation vector (MTV) to push the character out of the wall along the shortest path, ensuring they end up in a valid, non-colliding position.

## Tips

A common and frustrating bug in game development that requires a good understanding of physics and geometry.
