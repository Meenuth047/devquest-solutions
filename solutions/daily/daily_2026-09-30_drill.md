# DevQuest Solution: ⚡ Today's Drill: Extract Hex Color Codes (Regex) (2026-09-30)

- **Track**: 🔥 Daily Quests
- **Difficulty**: Beginner
- **Completed**: 2026-09-30 04:03:28 UTC
- **XP Earned**: +40 pts

---

## Problem Statement

**📅 Date:** `2026-09-30` | **⚡ Speed Drill**

### ⚡ Daily Drill: Hex Color Extractor (Regex)

Write a regular expression to match and extract 6-character or 3-character Hex color codes.
For example: `#ff007f` or `#fff`.

---

## Verified Solution (regex)

```regex
PATTERN = r"#[0-9a-fA-F]{6}|#[0-9a-fA-F]{3}"
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
