# LEETCODE-Strings-1910
### Dry Run:

1. **Initial Setup**:
   - `StringBuilder sb = new StringBuilder("daabcbaabcbc");`
   - `part = "abc"`

---

2. **First Iteration** of the `while` loop:
   - Condition: `sb.indexOf("abc") != -1` → `sb.indexOf("abc") = 2` (substring "abc" starts at index 2).
   - `si = 2`
   - Action: `sb.delete(2, 2 + 3)` → Removes characters from index 2 to 5 (length of "abc" is 3).
   - `sb = "dabaabcbc"`

---

3. **Second Iteration** of the `while` loop:
   - Condition: `sb.indexOf("abc") != -1` → `sb.indexOf("abc") = 4` (substring "abc" starts at index 4).
   - `si = 4`
   - Action: `sb.delete(4, 4 + 3)` → Removes characters from index 4 to 7.
   - `sb = "dababc"`

---

4. **Third Iteration** of the `while` loop:
   - Condition: `sb.indexOf("abc") != -1` → `sb.indexOf("abc") = 3` (substring "abc" starts at index 3).
   - `si = 3`
   - Action: `sb.delete(3, 3 + 3)` → Removes characters from index 3 to 6.
   - `sb = "dab"`

---

5. **Exit Loop**:
   - Condition: `sb.indexOf("abc") != -1` → `sb.indexOf("abc") = -1` (substring "abc" no longer exists in `sb`).
   - The loop terminates.

---

6. **Return Result**:
   - `return sb.toString();`
   - Final result: `"dab"`

---

### Output:
```java
"dab"
```

---

### Explanation:
- In each iteration, the method identifies the starting index of the first occurrence of `part` (`abc`) in the string and deletes it.
- The process repeats until all occurrences of `part` are removed from the string.
