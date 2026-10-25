---
title: "ECC Rule: C# Testing"
slug: ecc-rule-c-testing-1
stage: Test
category: "Testing & QA"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-rule-c-testing-1
---
# ECC Rule: C# Testing

Get C# testing conventions for xUnit, mocking, API integration tests, and coverage when adding unit or integration tests to a project.

## Prompt

# C# Testing

> This file extends [common/testing.md](../common/testing.md) with C#-specific content.

## Test Framework

- Prefer **xUnit** for unit and integration tests
- Use **FluentAssertions** for readable assertions
- Use **Moq** or **NSubstitute** for mocking dependencies
- Use **Testcontainers** when integration tests need real infrastructure

## Test Organization

- Mirror `src/` structure under `tests/`
- Separate unit, integration, and end-to-end coverage clearly
- Name tests by behavior, not implementation details

```csharp
public sealed class OrderServiceTests
{
    [Fact]
    public async Task FindByIdAsync_ReturnsOrder_WhenOrderExists()
    {
        // Arrange
        // Act
        // Assert
    }
}
```

## ASP.NET Core Integration Tests

- Use `WebApplicationFactory<TEntryPoint>` for API integration coverage
- Test auth, validation, and serialization through HTTP, not by bypassing middleware

## Coverage

- Target 80%+ line coverage
- Focus coverage on domain logic, validation, auth, and failure paths
- Run `dotnet test` in CI with coverage collection enabled where available

## Tips

Source: Everything Claude Code (ECC) — Rule: csharp/testing
