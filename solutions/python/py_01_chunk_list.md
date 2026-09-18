# DevQuest Solution: Fix the Sublist Chunker

- **Track**: Python
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 12:04:46 UTC
- **XP Earned**: +30 pts

---

## Problem Statement

### 🐛 Bug Hunt: `chunk_list(items, chunk_size)`

You are given a function that is supposed to partition a list into chunks of length `chunk_size`. The final chunk may be shorter than `chunk_size` if elements don't divide evenly.

**The Bug:** The current implementation uses an incorrect while-loop condition or slice calculation that drops the leftover trailing elements or loops infinitely!

**Task:** Fix `chunk_list` so that all items are partitioned correctly.

---

## Verified Solution (python)

```python
def chunk_list(items: list, chunk_size: int) -> list[list]:
    # BUG: drops leftover elements when len(items) % chunk_size != 0
    result = []
    for i in range(0, len(items) - chunk_size + 1, chunk_size):
        result.append(items[i : i + chunk_size])
    return result
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
