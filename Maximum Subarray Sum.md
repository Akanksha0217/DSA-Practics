# 🚀 Question

Maximum Subarray Sum (Kadane’s Algorithm)

# 🧠 Problem

Given:

arr = [-2,1,-3,4,-1,2,1,-5,4]

👉 Find maximum sum of a contiguous subarray

✅ Output
6

## Solution
### Using Python
```
arr = [-2,1,-3,4,-1,2,1,-5,4]

current_sum = arr[0]
max_sum = arr[0]

for i in range(1, len(arr)):
    current_sum = max(arr[i], current_sum + arr[i])
    max_sum = max(max_sum, current_sum)

print(max_sum)
```

### Using Js
```
let arr = [-2,1,-3,4,-1,2,1,-5,4];

let currentSum = arr[0];
let maxSum = arr[0];

for (let i = 1; i < arr.length; i++) {
  currentSum = Math.max(arr[i], currentSum + arr[i]);
  maxSum = Math.max(maxSum, currentSum);
}

console.log(maxSum);
```
