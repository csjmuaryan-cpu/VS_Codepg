# 2169. Count Operations to Obtain Zero — Notes

<aside>
🧩

Solved • Easy • Math, Simulation — Track reasoning, approach, code, and tests for quick revision.

</aside>

## Header

- **Problem Title:** 2169. Count Operations to Obtain Zero
- **Platform:** LeetCode
- **Link:** [Problem https://leetcode.com/problems/count-operations-to-obtain-zero](https://leetcode.com/problems/count-operations-to-obtain-zero) · [Accepted](https://leetcode.com/submissions/detail/1474326733/)
- **Difficulty:** Easy
- **Topic Tags:** Math, Simulation, Euclidean Algorithm
- **Date:** November 9, 2025
- **Status:** Solved

### Submission meta

- First occurrence: 01/13/25
- Age since first occurrence: 0 years, 9 months, 27 days, 10 hours, 05 minutes, 56 seconds
- Verdict: [Accepted](https://leetcode.com/submissions/detail/1474326733/)
- Runtime: 0 ms
- Language: C++
- Extra tag(s): Dynamic Programming
- Source repo: [github.com/Notes503](http://github.com/Notes503)

### Problem Statement (in my words)

Given non‑negative integers `num1` and `num2`, repeatedly subtract the smaller from the larger (or equal from equal) until one becomes 0. Count how many operations this takes. Return that count.

### Examples

- Input: num1 = 2, num2 = 3 → Output: 3
- Input: num1 = 10, num2 = 10 → Output: 1

---

# Notes

## 1. Problem understanding

- **Task:** Count the number of subtract operations until one number is 0.
- **Inputs:** Two integers in [0, 1e5].
- **Outputs:** Integer count of operations.
- **Goal:** Minimize time by batching repeated subtractions.

## 2. Key observations

- Repeated subtraction of the smaller from the larger is equivalent to integer division batching.
- If `a >= b`, then instead of subtracting `b` one by one, we can do `q = a // b` operations at once and reduce to `(a % b, b)`.
- This is exactly the Euclidean algorithm structure; the answer equals the sum of quotients encountered during GCD(a, b).
- Edge cases: if either is 0 initially, answer is 0.

## 3. Edge cases

- `a = 0` or `b = 0` → 0 operations.
- `a = b` and both > 0 → exactly 1 operation.
- Large but equal numbers → 1.
- One very large, one small → dominated by `a // b`.

## 4. Time/space complexity targets

- **Ideal Time Complexity:** O(log min(a, b)) using Euclid-style loop.
- **Ideal Space Complexity:** O(1).
- **Constraints:** Inputs up to 1e5, trivial for O(log n).

---

# Approach

## 1. Strategy outline

- Batch subtractions using division.
- While both numbers are nonzero:
    - If `a < b`, swap so `a >= b`.
    - `ops += a // b`, then `a %= b`.
- Return `ops`.
- **Initial thoughts:** Naive loop subtracting 1 at a time can be O(a + b) in worst cases; batching drops it to O(log n).
- **Key insight:** Sum of floor quotients in Euclid equals number of repeated subtractions.
- **Overall plan:** Implement the Euclid loop adding quotients to the answer.

## 2. Data structures

- Primitive integers only.

## 3. Algorithm steps

1. If `a == 0 or b == 0`, return 0.
2. Ensure `a >= b` by swapping if needed.
3. `ops += a // b`, `a %= b`.
4. Repeat until `b == 0`.
5. Return `ops`.

## 4. Complexity analysis

- **Time:** O(log min(a, b)) due to Euclidean reduction.
- **Space:** O(1).

---

# Solutions

## Python

```python
class Solution:
    def countOperations(self, num1: int, num2: int) -> int:
        a, b = num1, num2
        ops = 0
        while a and b:
            if a < b:
                a, b = b, a
            ops += a // b
            a %= b
        return ops
```

## C++

```cpp
class Solution {
public:
    int countOperations(int num1, int num2) {
        long long a = num1, b = num2; // safe though ints suffice
        long long ops = 0;
        while (a && b) {
            if (a < b) swap(a, b);
            ops += a / b;
            a %= b;
        }
        return (int)ops;
    }
};
```

## JavaScript

```jsx
var countOperations = function(num1, num2) {
  let a = num1, b = num2, ops = 0;
  while (a && b) {
    if (a < b) [a, b] = [b, a];
    ops += Math.floor(a / b);
    a = a % b;
  }
  return ops;
};
```

### Tests You Ran

- [ ]  Base case: a=0, b=5 → 0
- [ ]  Equal: a=10, b=10 → 1
- [ ]  Sample: a=2, b=3 → 3
- [ ]  Skewed: a=100000, b=1 → 100000
- [ ]  Random small pairs

### Mistakes and Fixes

- Watch for forgetting to add quotient when `a < b` before swapping.

### Similar / Follow-ups

- Relation to GCD and Euclidean algorithm.
- Variants: minimize operations with custom cost, or different operation rules.

### Revision Plan

- [ ]  Re-solve in 24 hours
- [ ]  Re-solve in 3 days
- [ ]  Re-solve in 1 week
- [ ]  Convert to another language