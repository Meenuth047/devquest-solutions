# DevQuest Solution: Deep Flatten Arbitrary Nesting

- **Track**: Python
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 11:27:59 UTC
- **XP Earned**: +50 pts

---

## Problem Statement

### 🛠️ Function Build: `deep_flatten(nested)`

Write a function `deep_flatten(nested)` that takes an arbitrarily deeply nested collection (composed of lists and tuples) and returns a flat list containing all the primitive values in their original order.

Strings should be treated as leaf values, not iterated character-by-character!

---

## Verified Solution (python)

```python
def deep_flatten(nested) -> list:
    result = []

    def flatten(item):
        if isinstance(item, (list, tuple)):
            for value in item:
                flatten(value)
        else:
            result.append(item)

    flatten(nested)
    return result
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
