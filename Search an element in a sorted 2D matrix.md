# 🚀 Question

Search an element in a sorted 2D matrix

# 🧠 Problem

Given matrix:
[
 [1, 3, 5],
 [7, 9, 11],
 [13, 15, 17]
]
👉 Find if target exists:

target = 9

# Solution
## Using Python Method 1
```
m = [
 [1, 3, 5],
 [7, 9, 11],
 [13, 15, 17]
]

target = 9

n = len(m)
p = len(m[0])

present = False

for i in range(n):
    for j in range(p):
        if m[i][j] == target:
            present = True
            break  # break inner loop
    if present:
        break  # break outer loop

print(present)
```
## Using JS
```
let m=[
 [1, 3, 5],
 [7, 9, 11],
 [13, 15, 17]
]

let target=9
n=m.length
p=m[0].length

let present=false

for(let i=0;i<n;i++){
    for(let j=0;j<p;j++){
        if(m[i][j]==target){
            present=true
            break
        }
    }
    if(present) break
}

console.log(present)
```

## Using Python Method 2
```
matrix = [
 [1, 3, 5],
 [7, 9, 11],
 [13, 15, 17]
]

target = 9

rows = len(matrix)
cols = len(matrix[0])

left = 0
right = rows * cols - 1

found = False

while left <= right:
    mid = (left + right) // 2

    row = mid // cols
    col = mid % cols

    if matrix[row][col] == target:
        found = True
        break
    elif matrix[row][col] < target:
        left = mid + 1
    else:
        right = mid - 1

print(found)
```
