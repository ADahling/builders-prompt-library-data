---
title: "Smart Contract Security: Reentrancy Attack"
slug: smart-contract-security-reentrancy-attack
stage: Secure
category: "Security Checklist"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/smart-contract-security-reentrancy-attack
---
# Smart Contract Security: Reentrancy Attack

Implement a secure withdrawal pattern to prevent reentrancy vulnerabilities by applying checks-effects-interactions and guard modifiers.

Variables: smart_contract_language

## Prompt

You are a smart contract developer who is writing a contract that handles user funds. You are aware of the reentrancy attack that led to the infamous DAO hack. Your task is to write a secure function for withdrawing funds that is not vulnerable to a reentrancy attack.

Context:
- The smart contract is written in `{{smart_contract_language}}` (e.g., Solidity).
- The contract has a mapping that stores the balance of each user.

Provide:
1. An explanation of what a reentrancy attack is and how it works, with a simple code example of a vulnerable `withdraw` function.
2. A secure version of the `withdraw` function that uses the 'checks-effects-interactions' pattern to prevent reentrancy attacks.
3. A brief explanation of other techniques to prevent reentrancy attacks, such as using a reentrancy guard (e.g., OpenZeppelin's `ReentrancyGuard`).

## Tips

An essential and practical prompt for any smart contract developer working with user funds.
