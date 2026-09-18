# DevQuest Solution: Extract Markdown Link URLs

- **Track**: Regex
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 11:30:00 UTC
- **XP Earned**: +40 pts

---

## Problem Statement

### 🎯 Regex Extraction: Markdown Hyperlinks

Given text containing markdown hyperlinks in the format `[Anchor Text](https://example.com/path)`, write a regex pattern that extracts the URL inside the parentheses as the first capturing group `(...)`.

Anchor text can contain any character except closing square brackets `]`, and the URL contains no closing parentheses `)`.

---

## Verified Solution (regex)

```regex
# TODO: Write a pattern with a capturing group for the URL inside ()
PATTERN = r"\[[^\]]*\]\(([^)]*)\)"
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
