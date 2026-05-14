# 🚀 Question

Binary Tree Level Order Traversal

## Problem

Tree:

       3
      / \
     9   20
        /  \
       15   7

Return nodes level by level.

## Solution
### Using Python
```
from collections import deque

def levelOrder(root):
    if not root:
        return []

    result = []
    queue = deque([root])

    while queue:
        level = []

        for _ in range(len(queue)):
            node = queue.popleft()

            level.append(node.val)

            if node.left:
                queue.append(node.left)

            if node.right:
                queue.append(node.right)

        result.append(level)

    return result
```
