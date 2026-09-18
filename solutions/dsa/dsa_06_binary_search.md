# DevQuest Solution: Day 6: Divide & Conquer (Binary Search)

- **Track**: DSA
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 12:01:35 UTC
- **XP Earned**: +50 pts

---

## Problem Statement

### 🧠 DSA Day 6: Binary Search ($O(\log N)$ Speed)

**Concept: Halving the Search Space**
If a list is **already sorted**, you don't need to inspect every item from left to right!
Imagine opening a dictionary in the middle:
- If the word you want comes alphabetically after the middle, discard the left half.
- If it comes before, discard the right half.

**Task:**
Given a sorted array `nums` and a `target`, return the index of `target`, or `-1` if it is not present.

---

## Verified Solution (python)

```python
def binary_search(nums: list[int], target: int) -> int:
    low = 0
    high = len(nums) - 1

    while low <= high:
        mid = (low + high) // 2

        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            low = mid + 1
        else:
            high = mid - 1

    return -1
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
