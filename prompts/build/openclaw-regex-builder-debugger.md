---
title: "OpenClaw: Regex Builder & Debugger"
slug: openclaw-regex-builder-debugger
stage: Build
category: "OpenClaw"
grade: A+
score: 98
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-regex-builder-debugger
---
# OpenClaw: Regex Builder & Debugger

Build a regex from a plain-language description and examples, with a breakdown of each part and a table of expected and actual matches.

Variables: description, examples, counter_examples

## Prompt

# Regex Builder & Debugger

## Input
Describe what you want to match in plain English:
"{{description}}"

Example inputs to match: {{examples}}
Example inputs to NOT match: {{counter_examples}}

## Output

### Generated Regex
```
/your-regex-here/flags
```

### Explanation (plain English)
Break down each part of the regex:
- `^` — Start of string
- `[A-Za-z]` — Any letter
- etc.

### Test Results
| Input | Expected | Actual | Match Groups |
|-------|----------|--------|-------------|
| "test@email.com" | ✅ Match | ✅ Match | ["test", "email", "com"] |
| "invalid" | ❌ No match | ❌ No match | — |

## Common Patterns Library

### Validation
| Pattern | Regex | Notes |
|---------|-------|-------|
| Email (basic) | `/^[^\s@]+@[^\s@]+\.[^\s@]+$/` | Not RFC 5322 compliant |
| URL | `/^https?:\/\/[^\s/$.?#].[^\s]*$/` | HTTP/HTTPS only |
| Phone (US) | `/^\+?1?[-.\s]?\(?[0-9]{3}\)?[-.\s]?[0-9]{3}[-.\s]?[0-9]{4}$/` | Flexible formatting |
| UUID v4 | `/^[0-9a-f]{8}-[0-9a-f]{4}-4[0-9a-f]{3}-[89ab][0-9a-f]{3}-[0-9a-f]{12}$/i` | Strict v4 |
| Hex color | `/^#([0-9A-Fa-f]{3}){1,2}$/` | 3 or 6 digit |
| Semver | `/^(0|[1-9]\d*)\.(0|[1-9]\d*)\.(0|[1-9]\d*)(-[\w.]+)?(\+[\w.]+)?$/` | Major.Minor.Patch |

### Extraction
| Pattern | Regex | Captures |
|---------|-------|----------|
| Date (ISO) | `/(\d{4})-(\d{2})-(\d{2})/` | Year, Month, Day |
| IP Address | `/(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/` | Octets |
| Log level | `/\[(ERROR|WARN|INFO|DEBUG)\]/` | Level |

## Performance Tips
- Avoid catastrophic backtracking: no nested quantifiers `(a+)+`
- Use non-capturing groups `(?:...)` when you don't need the match
- Anchor patterns with `^` and `$` when matching full strings
- Prefer possessive quantifiers or atomic groups when available

## Tips

Builds and debugs regex from plain English descriptions. Includes common pattern library, test results, and performance tips.
