# 🚀 Question

Number of Islands

# 🧠 Problem

Given grid:

grid = [
 ["1","1","0","0","0"],
 ["1","1","0","0","0"],
 ["0","0","1","0","0"],
 ["0","0","0","1","1"]
]

👉 Count number of islands

🧠 What is island?

👉 Connected 1s (land)

👉 Connected by:

up
down
left
right

# Solution
## Using Python

```
grid = [
 ["1","1","0","0","0"],
 ["1","1","0","0","0"],
 ["0","0","1","0","0"],
 ["0","0","0","1","1"]
]

rows = len(grid)
cols = len(grid[0])

def dfs(r, c):
    if r < 0 or c < 0 or r >= rows or c >= cols or grid[r][c] == "0":
        return

    grid[r][c] = "0"

    dfs(r+1, c)
    dfs(r-1, c)
    dfs(r, c+1)
    dfs(r, c-1)

count = 0

for i in range(rows):
    for j in range(cols):
        if grid[i][j] == "1":
            count += 1
            dfs(i, j)

print(count)

```

## Using Js
```
let grid = [
 ["1","1","0","0","0"],
 ["1","1","0","0","0"],
 ["0","0","1","0","0"],
 ["0","0","0","1","1"]
];

let rows = grid.length;
let cols = grid[0].length;

function dfs(r, c) {
  if (
    r < 0 || c < 0 ||
    r >= rows || c >= cols ||
    grid[r][c] === "0"
  ) return;

  grid[r][c] = "0";

  dfs(r + 1, c);
  dfs(r - 1, c);
  dfs(r, c + 1);
  dfs(r, c - 1);
}

let count = 0;

for (let i = 0; i < rows; i++) {
  for (let j = 0; j < cols; j++) {
    if (grid[i][j] === "1") {
      count++;
      dfs(i, j);
    }
  }
}

console.log(count);
```
