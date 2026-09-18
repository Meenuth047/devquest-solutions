# DevQuest Solution: Day 1: Array Traversal & Running Sum

- **Track**: DSA
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 11:52:32 UTC
- **XP Earned**: +30 pts

---

## Problem Statement

### 🧠 DSA Day 1: Understanding Arrays & Prefix Sums

**Concept: What is an Array?**
An array (or Python list) is an ordered collection of elements. To build algorithmic muscle memory, the most fundamental operation is **traversal** (visiting each item one by one).

**Problem:**
Given an array of numbers `nums`, return a new array where each element at index `i` is the sum of all elements from index `0` through `i`.

```
Input:  [1, 2, 3, 4]
Output: [1, 3, 6, 10]
Explanation:
  Index 0: 1
  Index 1: 1 + 2 = 3
  Index 2: 1 + 2 + 3 = 6
  Index 3: 1 + 2 + 3 + 4 = 10
```

**Time Complexity Goal:** $O(N)$ with a single loop.

---

## Verified Solution (python)

```python
def running_sum(nums: list[int]) -> list[int]:
    # TODO: Create a running sum accumulator and iterate through nums
    result = []
    current_sum = 0

    for x in nums:
        current_sum += x
        result.append(current_sum)

    return result
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
