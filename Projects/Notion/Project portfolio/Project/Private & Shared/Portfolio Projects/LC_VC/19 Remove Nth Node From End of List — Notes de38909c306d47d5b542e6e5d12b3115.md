# 19. Remove Nth Node From End of List — Notes

<aside>
🧩

Solved • Medium • Linked List, Two Pointers — One-pass fast/slow pointer with dummy head.

</aside>

## Header

- **Problem Title:** 19. Remove Nth Node From End of List
- **Platform:** LeetCode
- **Link:** [Problem https://leetcode.com/problems/remove-nth-node-from-end-of-list/](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) · [Canonical](https://leetcode.com/problems/remove-nth-node-from-end-of-list) · [Accepted](https://leetcode.com/submissions/detail/1535685331/)
- **Difficulty:** Medium
- **Topic Tags:** Linked List, Two Pointers, Deletion
- **Date:** February 12, 2025
- **Status:** Solved

### Submission meta

- First occurrence: 02/12/25
- Age since first occurrence: 0 years, 8 months, 28 days, 10 hours, 21 minutes, 29 seconds
- Verdict: [Accepted](https://leetcode.com/submissions/detail/1535685331/)
- Runtime: 0 ms
- Language: C++
- Extra tag(s): Linked List Manipulation / Deletion
- Source repo: [github.com/Notes19](http://github.com/Notes19)

---

# Notes

## 1. Problem understanding

Remove the nth node from the end and return head.

- **Inputs:** `head` (singly linked list), `n` in [1..sz].
- **Output:** new list head after deletion.
- **Goal:** Prefer one pass, O(1) extra space.

## 2. Key observations

- Use a dummy node before head to unify deletion of the first node.
- Keep two pointers `fast` and `slow` at dummy. Advance `fast` by `n+1` steps so the gap is `n`.
- Move both until `fast` hits null. `slow` stops before the node to delete. Splice `slow->next`.

## 3. Edge cases

- Deleting the head itself (n == sz) handled by dummy.
- sz within 1..30, values 0..100.

## 4. Time/space complexity targets

- **Time:** O(sz)
- **Space:** O(1)

---

# Approach

## 1. Strategy outline

One-pass two-pointer with dummy:

1. Create `dummy->next = head`.
2. Move `fast` `n+1` steps from dummy.
3. While `fast` not null, move both `fast` and `slow`.
4. Delete `slow->next` by `slow->next = slow->next->next`.
5. Return `dummy->next`.

## 2. Data structures

- Dummy node, two pointers.

## 3. Algorithm steps

1. Initialize `dummy`, `fast = slow = dummy`.
2. For i in 0..n: `fast = fast->next`.
3. While `fast != null`: advance both.
4. Splice `slow->next`.
5. Return `dummy->next`.

## 4. Complexity analysis

- **Time:** O(sz)
- **Space:** O(1)

---

# Solutions

## Python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         [self.next](http://self.next) = next
class Solution:
    def removeNthFromEnd(self, head: Optional[ListNode], n: int) -> Optional[ListNode]:
        dummy = ListNode(0, head)
        fast = slow = dummy
        for _ in range(n + 1):
            fast = [fast.next](http://fast.next)
        while fast:
            fast = [fast.next](http://fast.next)
            slow = [slow.next](http://slow.next)
        [slow.next](http://slow.next) = [slow.next.next](http://slow.next.next)
        return [dummy.next](http://dummy.next)
```

## C++

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* removeNthFromEnd(ListNode* head, int n) {
        ListNode dummy(0, head);
        ListNode *fast = &dummy, *slow = &dummy;
        for (int i = 0; i <= n; ++i) fast = fast->next; // n+1 steps
        while (fast) { fast = fast->next; slow = slow->next; }
        slow->next = slow->next->next;
        return [dummy.next](http://dummy.next);
    }
};
```

## JavaScript

```jsx
/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *   this.val = (val===undefined ? 0 : val)
 *   [this.next](http://this.next) = (next===undefined ? null : next)
 * }
 */
var removeNthFromEnd = function(head, n) {
  const dummy = { val: 0, next: head };
  let fast = dummy, slow = dummy;
  for (let i = 0; i <= n; i++) fast = [fast.next](http://fast.next);
  while (fast) { fast = [fast.next](http://fast.next); slow = [slow.next](http://slow.next); }
  [slow.next](http://slow.next) = [slow.next.next](http://slow.next.next);
  return [dummy.next](http://dummy.next);
};
```

### Tests You Ran

- [ ]  [1,2,3,4,5], n=2 → [1,2,3,5]
- [ ]  [1], n=1 → []
- [ ]  [1,2], n=1 → [1]
- [ ]  delete first node case (n == sz)

### Mistakes and Fixes

- Off-by-one in advancing fast; ensure `n+1` steps from dummy.

### Similar / Follow-ups

- Multi-pass version: length then delete `len-n+1`.
- Variation: return both new head and deleted value.

### Revision Plan

- [ ]  Re-solve in 24 hours
- [ ]  Re-solve in 3 days
- [ ]  Re-solve in 1 week
- [ ]  Convert to another language