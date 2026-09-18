# DevQuest Solution: Unix Permissions Translator

- **Track**: Linux
- **Difficulty**: Beginner
- **Completed**: 2026-09-18 11:12:25 UTC
- **XP Earned**: +30 pts

---

## Problem Statement

### 🐧 Linux Skills: Symbolic to Octal Permissions

In Unix systems, permissions are represented in symbolic form like `rwxr-xr--`.
Each triad corresponds to User, Group, and Others where:
- `r` = 4 (Read)
- `w` = 2 (Write)
- `x` = 1 (Execute)
- `-` = 0 (No permission)

**Task:** Write a Python function `symbolic_to_octal(perm_str: str) -> str` that converts a 9-character permission string (e.g. `'rwxr-xr--'`) into its 3-digit octal string representation (e.g. `'754'`).

---

## Verified Solution (python)

```python
def symbolic_to_octal(perm: str) -> str:
    # Convert a 9-char symbolic permission (e.g. 'rwxr-xr--') to octal ('754')
    values = {'r': 4, 'w':2, 'x': 1, '-': 0}

    result = []

    for i in range(0, 9, 3):
        total = values[perm[i]] + values[perm[i + 1]] + values[perm[i + 2 ]]
        result.append(str(total))
    return ''.join(result)
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
