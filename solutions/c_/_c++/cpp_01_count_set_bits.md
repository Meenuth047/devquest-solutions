# DevQuest Solution: Brian Kernighan's Bit Counter

- **Track**: C / C++
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 11:55:26 UTC
- **XP Earned**: +45 pts

---

## Problem Statement

### ⚙️ C / C++: Bit Manipulation

**Brian Kernighan's Algorithm:**
Subtracting `1` from an integer flips all the bits to the right of the lowest set bit (including that bit).
Therefore, doing bitwise AND `n = n & (n - 1)` clears the lowest set bit in each iteration!

**Task:** Write a function `count_set_bits(n: int) -> int` that returns the number of set bits (`1`s) in `n`'s binary representation.

---

## Verified Solution (python)

```python
def count_set_bits(n: int) -> int:
    count = 0
    while n > 0:
        n &= (n - 1)  # Clears the least significant set bit
        count += 1
    return count
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
