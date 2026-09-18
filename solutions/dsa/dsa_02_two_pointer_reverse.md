# DevQuest Solution: Day 2: Two-Pointer Technique (Reverse List)

- **Track**: DSA
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 11:54:26 UTC
- **XP Earned**: +35 pts

---

## Problem Statement

### 🧠 DSA Day 2: The Two-Pointer Technique

**Concept: Why Two Pointers?**
Instead of creating a whole new array (which wastes memory / $O(N)$ space), we can place two markers:
- One pointer at the **start** (`left = 0`)
- One pointer at the **end** (`right = len - 1`)

By swapping the elements at `left` and `right`, then incrementing `left` and decrementing `right`, we reverse the list **in-place** with $O(1)$ extra memory!

**Task:** Implement `reverse_list(items)` to reverse the list in-place and return it.

---

## Verified Solution (python)

```python
def reverse_list(items: list) -> list:
    left = 0
    right = len(items) - 1

    while left < right:
        items[left], items[right] = items[right], items[left]
        left += 1
        right -= 1

    return items
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
