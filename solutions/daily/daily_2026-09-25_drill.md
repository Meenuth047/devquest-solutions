# DevQuest Solution: ⚡ Today's Drill: Extract Markdown Image URLs (Regex) (2026-09-25)

- **Track**: 🔥 Daily Quests
- **Difficulty**: Beginner
- **Completed**: 2026-09-25 07:05:03 UTC
- **XP Earned**: +40 pts

---

## Problem Statement

**📅 Date:** `2026-09-25` | **⚡ Speed Drill**

### ⚡ Daily Drill: Markdown Image Extractor (Regex)

Write a regular expression that captures the image URL from Markdown image tags: `![alt](url)`.
Capture Group (1): The image URL.

---

## Verified Solution (regex)

```regex
PATTERN = r"!\[.*?\]\((https?://[^\s\)]+)\)"
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
