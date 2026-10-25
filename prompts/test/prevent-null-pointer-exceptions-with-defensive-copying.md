---
title: "Prevent Null Pointer Exceptions with Defensive Copying"
slug: prevent-null-pointer-exceptions-with-defensive-copying
stage: Test
category: "Critical Bugs"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/prevent-null-pointer-exceptions-with-defensive-copying
---
# Prevent Null Pointer Exceptions with Defensive Copying

Secure Java class integrity by implementing defensive copying for mutable objects to prevent accidental or malicious internal state mutation.

## Prompt

You are a Java developer writing a library. You have a class that takes a mutable object (like a `Date` or a `List`) in its constructor and stores it in a private field. You have discovered that clients of your class can modify the internal state of your object after it has been created by mutating the object they passed to the constructor. Your task is to make your class immutable and safe from this.

Context:
- The class is supposed to be immutable, meaning its state should not change after creation.
- A malicious or careless caller can pass a `Date` object to the constructor, and then later call `setDate()` on that same object, which changes the internal state of your class.

Provide:
1. A Java class that is vulnerable to this problem.
2. An explanation of the problem, which is that the constructor is storing an alias to a mutable object.
3. The corrected constructor that performs a ‘defensive copy’ of the mutable object. For a `Date` object, this would mean creating a `new Date(original.getTime())` and storing the copy instead of the original.

## Tips

An important concept for writing robust and secure libraries, as described in Joshua Bloch’s ‘Effective Java’.
