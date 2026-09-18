# DevQuest Solution: High-Value Customers

- **Track**: SQL
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 11:30:27 UTC
- **XP Earned**: +35 pts

---

## Problem Statement

### 🔍 SQL Detective: Top Spenders

We have two tables: `customers` (`id`, `name`, `country`) and `orders` (`id`, `customer_id`, `amount`, `order_date`).

**Task:** Write a query that returns each customer's `name` and their total order amount as `total_spent`.
- Only include customers whose total spending is **greater than $100**.
- Order the results by `total_spent` in **descending** order.

**Expected columns:** `name`, `total_spent`

---

## Verified Solution (sql)

```sql
-- Write your SQL query below:
SELECT c.name, SUM(o.amount) AS total_spent
FROM customers c
JOIN orders o ON c.id = o.customer_id
GROUP BY c.id, c.name
HAVING SUM(o.amount) > 100
ORDER BY total_spent DESC;
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
