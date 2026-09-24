# DevQuest Solution: ⚡ Today's Drill: Customers Who Never Order (SQL) (2026-09-24)

- **Track**: 🔥 Daily Quests
- **Difficulty**: Beginner
- **Completed**: 2026-09-24 11:15:41 UTC
- **XP Earned**: +45 pts

---

## Problem Statement

**📅 Date:** `2026-09-24` | **⚡ Speed Drill**

### ⚡ Daily Drill: Customers Without Orders (SQL)

Tables `Customers` (columns `id`, `name`) and `Orders` (columns `id`, `customerId`).
Write a query to report all customers who never placed an order. Return their `name`.

---

## Verified Solution (sql)

```sql
-- Find customers without any order:
SELECT name
FROM Customers
WHERE id NOT IN (SELECT customerId FROM Orders);
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
