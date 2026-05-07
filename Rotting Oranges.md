# Rotting Oranges

## 🧠 Problem

Grid:
```
[
 [2,1,1],
 [1,1,0],
 [0,1,1]
]
```

### Meaning:

- 0 = empty
- 1 = fresh orange 🍊
- 2 = rotten orange 🤢

### Rule

Every minute:
```
Rotten orange infects nearby fresh oranges
```
Only:
- up
- down
- left
- right

## Solution
### Using Python
```
from collections import deque

grid = [
 [2,1,1],
 [1,1,0],
 [0,1,1]
]

rows = len(grid)
cols = len(grid[0])

queue = deque()
fresh = 0
minutes = 0

for r in range(rows):
    for c in range(cols):
        if grid[r][c] == 2:
            queue.append((r,c))

        elif grid[r][c] == 1:
            fresh += 1

dirs = [[1,0],[-1,0],[0,1],[0,-1]]

while queue and fresh > 0:

    for _ in range(len(queue)):
        r, c = queue.popleft()

        for dr, dc in dirs:
            nr = r + dr
            nc = c + dc

            if 0 <= nr < rows and 0 <= nc < cols and grid[nr][nc] == 1:

                grid[nr][nc] = 2
                fresh -= 1
                queue.append((nr,nc))

    minutes += 1

if fresh == 0:
    print(minutes)
else:
    print(-1)
```
