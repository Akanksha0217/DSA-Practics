# 🚀 Question: Set Matrix Zeroes
🧠 Problem

Given a matrix:

[
 [1,1,1],
 [1,0,1],
 [1,1,1]
]

👉 If any cell = 0
👉 Make entire row + column = 0

✅ Output
[
 [1,0,1],
 [0,0,0],
 [1,0,1]
]

# SOlution
## Using Python
```
matrix = [
    [1,1,1],
    [1,0,1],
    [1,1,1]
]

rows = len(matrix)
cols = len(matrix[0])

row_zero = [False] * rows
col_zero = [False] * cols

# Step 1: Mark rows & columns that have 0
for i in range(rows):
    for j in range(cols):
        if matrix[i][j] == 0:
            row_zero[i] = True
            col_zero[j] = True

# Step 2: Update matrix
for i in range(rows):
    for j in range(cols):
        if row_zero[i] or col_zero[j]:
            matrix[i][j] = 0

# Print result
for row in matrix:
    print(row)
```

## Using JS
```
let matrix = [
  [1,1,1],
  [1,0,1],
  [1,1,1]
];

let rows = matrix.length;
let cols = matrix[0].length;

let rowZero = new Array(rows).fill(false);
let colZero = new Array(cols).fill(false);

// Step 1: mark zeros
for (let i = 0; i < rows; i++) {
  for (let j = 0; j < cols; j++) {
    if (matrix[i][j] === 0) {
      rowZero[i] = true;
      colZero[j] = true;
    }
  }
}

// Step 2: update matrix
for (let i = 0; i < rows; i++) {
  for (let j = 0; j < cols; j++) {
    if (rowZero[i] || colZero[j]) {
      matrix[i][j] = 0;
    }
  }
}

console.log(matrix);
```
