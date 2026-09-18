# DevQuest Solution: Day 3: Hash Maps for O(1) Lookup (Two Sum)

- **Track**: DSA
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 11:55:53 UTC
- **XP Earned**: +40 pts

---

## Problem Statement

### 🧠 DSA Day 3: Fast Lookups with Hash Maps (Dictionaries)

**The Problem with Brute Force:**
Checking all pairs with nested loops takes $O(N^2)$ time—way too slow for big data!

**The Hash Map Solution:**
A dictionary gives **instant $O(1)$ key lookup**. As we loop through `nums`:
1. For each number `num`, the partner we need is `needed = target - num`.
2. If `needed` is already in our map, we found our pair! Return `[seen[needed], current_index]`.
3. Otherwise, remember current number: `seen[num] = current_index`.

**Task:** Return the indices of the two numbers that add up to `target`.

---

## Verified Solution (python)

```python
def two_sum(nums: list[int], target: int) -> list[int]:
    seen = {}

    for i, num in enumerate(nums):
        complement = target - num

        if complement in seen:
            return [seen[complement], i]

        seen[num] = i

    return []
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
