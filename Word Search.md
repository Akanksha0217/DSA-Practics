# 🚀 Question

Word Search

## 🧠 Problem

Given a grid:

board = [
 ['A','B','C','E'],
 ['S','F','C','S'],
 ['A','D','E','E']
]

word = "ABCCED"

👉 Check if the word exists in the grid

👉 You can move:

up ⬆️
down ⬇️
left ⬅️
right ➡️

👉 Cannot reuse same cell
✅ Output
True


## Solution
### Using Python
```
board = [
 ['A','B','C','E'],
 ['S','F','C','S'],
 ['A','D','E','E']
]

word = "B"

rows = len(board)
cols = len(board[0])
print(len(word))
def dfs(r, c, i):
    if i == len(word):
        return True

    if r < 0 or c < 0 or r >= rows or c >= cols or board[r][c] != word[i]:
        return False

    temp = board[r][c]
    board[r][c] = "#"

    found = (dfs(r+1, c, i+1) or
             dfs(r-1, c, i+1) or
             dfs(r, c+1, i+1) or
             dfs(r, c-1, i+1))

    board[r][c] = temp

    return found

for i in range(rows):
    for j in range(cols):
        if dfs(i, j, 0):
            print(True)
            exit()

print(False)
```

### SUing JS
```
let board = [
 ['A','B','C','E'],
 ['S','F','C','S'],
 ['A','D','E','E']
];

let word = "ABCCED";

let rows = board.length;
let cols = board[0].length;

function dfs(r, c, i) {
  if (i === word.length) return true;

  if (r < 0 || c < 0 || r >= rows || c >= cols || board[r][c] !== word[i]) {
    return false;
  }

  let temp = board[r][c];
  board[r][c] = "#";

  let found =
    dfs(r + 1, c, i + 1) ||
    dfs(r - 1, c, i + 1) ||
    dfs(r, c + 1, i + 1) ||
    dfs(r, c - 1, i + 1);

  board[r][c] = temp;

  return found;
}

let result = false;

for (let i = 0; i < rows; i++) {
  for (let j = 0; j < cols; j++) {
    if (dfs(i, j, 0)) {
      result = true;
    }
  }
}

console.log(result);
```

