# 🚀 Question

Remove Nth Node From End of Linked List

Problem
Linked list:
1 → 2 → 3 → 4 → 5
and
n = 2
Remove 2nd node from end.

## Solution
### Using Python
- Time Complexity :O(n)
- Space Complexity :O(1)
```
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next


def removeNth(head, n):
    dummy = ListNode(0)
    dummy.next = head

    fast = dummy
    slow = dummy

    for _ in range(n + 1):
        fast = fast.next

    while fast:
        fast = fast.next
        slow = slow.next

    slow.next = slow.next.next

    return dummy.next
```
