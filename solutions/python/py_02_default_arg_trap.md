# DevQuest Solution: The Mutable Default Argument Trap

- **Track**: Python
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 11:20:24 UTC
- **XP Earned**: +40 pts

---

## Problem Statement

### 🐛 Bug Hunt: The Sticky Cache

In Python, default parameter values are evaluated **once** when the function is defined, not each time the function is called. When using a mutable default like `cache=[]`, mutations persist across separate calls!

**Task:** Fix `add_to_registry` so each caller gets an isolated, fresh list if `registry` is not provided, while appending `entry` and returning the list.

---

## Verified Solution (python)

```python
def add_to_registry(entry: str, registry: list = None) -> list:
    if registry is None:
        registry = []
    registry.append(entry)
    return registry
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
