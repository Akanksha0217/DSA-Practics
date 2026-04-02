# 🚀 Question

Find the product of array except self

# 🧠 Problem

Given an array, return a new array where:

result[i] = product of all elements except arr[i]

# Solution
## Using Python
```
arr = [1, 2, 3, 4]
n = len(arr)

left = [0] * n
right = [0] * n
result = [0] * n

# Step 1: Left product
left[0] = 1
for i in range(1, n):
    left[i] = left[i - 1] * arr[i - 1]

# Step 2: Right product
right[n - 1] = 1
for i in range(n - 2, -1, -1):
    right[i] = right[i + 1] * arr[i + 1]

# Step 3: Final result
for i in range(n):
    result[i] = left[i] * right[i]

print(result)
```

## Using  Js
```
let arr = [1, 2, 3, 4];
let n = arr.length;

let left = new Array(n);
let right = new Array(n);
let result = new Array(n);

// left
left[0] = 1;
for (let i = 1; i < n; i++) {
  left[i] = left[i - 1] * arr[i - 1];
}

// right
right[n - 1] = 1;
for (let i = n - 2; i >= 0; i--) {
  right[i] = right[i + 1] * arr[i + 1];
}

// result
for (let i = 0; i < n; i++) {
  result[i] = left[i] * right[i];
}

console.log(result);

```
