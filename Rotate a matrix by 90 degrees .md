# 🚀 Question

Rotate a matrix by 90 degrees (clockwise)

## 🧠 Problem

Given:

matrix = [
 [1,2,3],
 [4,5,6],
 [7,8,9]
]
✅ Output
[
 [7,4,1],
 [8,5,2],
 [9,6,3]
]

# Solution

### Using Python
```
matrix = [
 [1,2,3],
 [4,5,6],
 [7,8,9]
]

n = len(matrix)

# Step 1: Transpose
for i in range(n):
    for j in range(i, n):
        matrix[i][j], matrix[j][i] = matrix[j][i], matrix[i][j]

# Step 2: Reverse rows
for row in matrix:
    row.reverse()

for row in matrix:
    print(row)
```


### Using Js
```
let matrix = [
 [1,2,3],
 [4,5,6],
 [7,8,9]
];

let n = matrix.length;

// Step 1: Transpose
for (let i = 0; i < n; i++) {
  for (let j = i; j < n; j++) {
    [matrix[i][j], matrix[j][i]] = [matrix[j][i], matrix[i][j]];
  }
}

// Step 2: Reverse each row
for (let row of matrix) {
  row.reverse();
}

console.log(matrix);
```
