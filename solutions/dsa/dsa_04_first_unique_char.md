# DevQuest Solution: Day 4: Frequency Counting (First Unique Character)

- **Track**: DSA
- **Difficulty**: Intermediate
- **Completed**: 2026-09-18 11:56:16 UTC
- **XP Earned**: +40 pts

---

## Problem Statement

### 🧠 DSA Day 4: Frequency Maps / Counting Pattern

**Concept: Two-Pass Strategy**
Many interview and real-world problems require counting how often items appear.
- **Pass 1:** Count the frequency of every character using a hash map or dictionary.
- **Pass 2:** Iterate through the string again and return the index of the first character whose frequency is `1`.

If no unique character exists, return `-1`.

**Example:**
`s = 'leetcode'` ➔ 'l' appears only once, index `0`.
`s = 'loveleetcode'` ➔ 'l' appears twice, 'o' appears twice, 'v' appears once ➔ index `2`.

---

## Verified Solution (python)

```python
def first_uniq_char(s: str) -> int:
    # Step 1: Count character frequencies
    counts = {}
    for ch in s:
        counts[ch] = counts.get(ch, 0) + 1

    # Step 2: Find the first character whose count is 1
    for i, ch in enumerate(s):
        if counts[ch] == 1:
            return i

    return -1
```

## Verification Status
- All automated test cases passed successfully.
- Tested with DevQuest TUI runner.
