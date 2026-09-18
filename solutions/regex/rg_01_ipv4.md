# DevQuest Solution: Validate IPv4 Addresses

- **Track**: Regex
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 11:29:22 UTC
- **XP Earned**: +30 pts

---

## Problem Statement

### 🎯 Regex Golf: Standard IPv4 Matcher

Write a regular expression pattern that matches a valid IPv4 address in dot-decimal notation: `X.X.X.X` where each octet `X` is between 0 and 255.

For this introductory challenge, match numbers from 0 to 255 across 4 dot-separated blocks. Leading zeros on multi-digit numbers (like `01` or `099`) should be rejected if possible, or standard octet range.

**Output format:** Simply return your regular expression pattern string.

---

## Verified Solution (regex)

```regex
# Enter your regex pattern (currently too naive - matches out-of-range octets):
PATTERN = r"^(?:(?:25[0-5]|2[0-4]\d|1\d\d|[1-9]?\d)\.){3}(?:25[0-5]|2[0-4]\d|1\d\d|[1-9]?\d)$"
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
