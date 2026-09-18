# DevQuest Solution: Day 7: Kadane's Algorithm (Max Subarray Sum)

- **Track**: DSA
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 12:02:19 UTC
- **XP Earned**: +55 pts

---

## Problem Statement

### 🧠 DSA Day 7: Dynamic Subarray Sums (Kadane's Algorithm)

**Problem:**
Given an integer array `nums`, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

**Kadane's Intuition:**
As we walk through the array, at each number `x`, we make a choice:
1. Either add `x` to our existing accumulated subarray sum (`current_sum + x`).
2. Or discard the past and start a brand new subarray starting at `x` (`x`).

Formula: `current_sum = max(x, current_sum + x)`
Keep tracking `max_so_far = max(max_so_far, current_sum)`.

---

## Verified Solution (python)

```python
def max_subarray(nums: list[int]) -> int:
    max_so_far = nums[0]
    current_sum = nums[0]

    for x in nums[1:]:
        current_sum = max(x, current_sum + x)
        max_so_far = max(max_so_far, current_sum)

    return max_so_far
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
