# DevQuest Solution: Day 5: Stacks (Valid Matching Brackets)

- **Track**: DSA
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 12:00:58 UTC
- **XP Earned**: +45 pts

---

## Problem Statement

### 🧠 DSA Day 5: Stacks (LIFO - Last-In, First-Out)

**Concept: Why a Stack?**
When checking nested structures like parentheses `()`, brackets `[]`, and braces `{}`, the most recently opened bracket must be the first one to close!

**Algorithm:**
1. Initialize an empty list `stack = []`.
2. When you encounter an opening bracket `(`, `[`, or `{`, push it onto the stack.
3. When you encounter a closing bracket, pop from the stack and verify that it matches the corresponding opening bracket.
4. At the end, the stack should be empty if all brackets matched cleanly.

---

## Verified Solution (python)

```python
def is_valid_parentheses(s: str) -> bool:
    matching = {')': '(', ']': '[', '}': '{'}
    stack = []

    for char in s:
        if char in '([{':
            stack.append(char)
        elif char in matching:
            if not stack or stack.pop() != matching[char]:
                return False

    return len(stack) == 0
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
