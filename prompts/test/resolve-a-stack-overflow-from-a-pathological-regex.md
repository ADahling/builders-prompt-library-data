---
title: "Resolve a Stack Overflow from a Pathological Regex"
slug: resolve-a-stack-overflow-from-a-pathological-regex
stage: Test
category: "Critical Bugs"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-a-stack-overflow-from-a-pathological-regex
---
# Resolve a Stack Overflow from a Pathological Regex

Diagnose and mitigate regex stack overflows by refactoring nested quantifiers or migrating to non-recursive engines like RE2.

## Prompt

You are a developer using a regex library that is implemented recursively, such as the one in some older versions of Perl or PCRE. You have a regex with nested quantifiers and a long input string that triggers a huge amount of recursion in the regex engine, leading to a stack overflow in your application.

Context:
- The regex is something like `(a*)*` which is a pathological case.
- The regex engine is trying to match this against a long string of ‘a’s.
- The recursive implementation of the regex engine consumes a stack frame for each level of recursion, and the number of ways to match this pattern is enormous.

Provide:
1. An explanation of how a recursive regex engine works and why certain patterns can lead to deep recursion and stack overflow.
2. An example of a pathological regex and an input string that would trigger this behavior.
3. A discussion of how to mitigate this. This includes rewriting the regex to be less ambiguous and avoiding nested quantifiers. It also involves choosing a regex engine that uses a non-recursive implementation (like Google’s RE2), which guarantees linear time execution and does not suffer from this problem.

## Tips

A deep dive into the implementation details of regular expression engines.
