# DevQuest Solution: ⚡ Today's Drill: Find Duplicate Emails (SQL) (2026-10-26)

- **Track**: 🔥 Daily Quests
- **Difficulty**: Beginner
- **Completed**: 2026-10-26 06:39:15 UTC
- **XP Earned**: +45 pts

---

## Problem Statement

**📅 Date:** `2026-10-26` | **⚡ Speed Drill**

### ⚡ Daily Drill: SQL Duplicate Detector

Table `users` has columns `id` and `email`.
Write a query to report all the duplicate emails. Return the `email` column.

---

## Verified Solution (sql)

```sql
-- Find emails that appear more than once:
SELECT email
FROM users
GROUP BY email
HAVING COUNT(email) > 1;
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
