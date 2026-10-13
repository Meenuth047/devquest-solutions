# DevQuest Solution: ⚡ Today's Drill: Second Highest Salary (SQL) (2026-10-13)

- **Track**: 🔥 Daily Quests
- **Difficulty**: Intermediate
- **Completed**: 2026-10-13 04:24:17 UTC
- **XP Earned**: +50 pts

---

## Problem Statement

**📅 Date:** `2026-10-13` | **⚡ Speed Drill**

### ⚡ Daily Drill: SQL Second Highest Salary

Table `Employee` has columns `id` and `salary`.
Write a SQL query to get the second highest distinct salary from the `Employee` table.
Return the column as `SecondHighestSalary`.

---

## Verified Solution (sql)

```sql
-- Return the 2nd highest distinct salary:
SELECT (SELECT DISTINCT salary FROM Employee ORDER BY salary DESC LIMIT 1 OFFSET 1) AS SecondHighestSalary;
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
