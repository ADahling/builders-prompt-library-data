---
title: "Security Review of a Web3 Application"
slug: security-review-of-a-web3-application
stage: Secure
category: "Security Review"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-review-of-a-web3-application
---
# Security Review of a Web3 Application

Conduct a comprehensive security audit of a Web3 dApp to identify vulnerabilities in smart contracts, frontend code, and key management.

Variables: dapp_name, blockchain_platform, smart_contract_language

## Prompt

You are a security researcher specializing in Web3 and blockchain applications. You have been asked to review a new decentralized application (dApp), {{dapp_name}}, which is built on the {{blockchain_platform}} blockchain. The dApp includes a smart contract written in {{smart_contract_language}} and a web-based frontend.

Create a detailed security review report in Markdown. The report should cover the following areas:

1.  **Smart Contract Security:**
    *   Are there any common smart contract vulnerabilities, such as reentrancy, integer overflow/underflow, or unchecked external calls?
    *   Is the smart contract code well-documented and easy to understand?
    *   Has the smart contract been audited by a third party?

2.  **Frontend Security:**
    *   How does the frontend interact with the user's wallet?
    *   Is the frontend vulnerable to common web vulnerabilities, such as XSS or CSRF?

3.  **Private Key Management:**
    *   How are users expected to manage their private keys?
    *   Does the dApp provide any guidance on secure key management?

4.  **Transaction Security:**
    *   Are transactions signed on the client side?
    *   Is there any protection against front-running or other transaction-related attacks?

For each area, provide your assessment and a list of prioritized recommendations for improvement. Your report should be a comprehensive guide for the development team to improve the security of their dApp.
