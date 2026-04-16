# Question

Find Longest Increasing Subsequence (LIS)

## 🧠 Problem

Given:

arr = [10,9,2,5,3,7,101,18]
✅ Output
4
👉 One LIS is:
[2,3,7,101]

## Solution
## Using Python
```
arr = [10,9,2,5,3,7,101,18]

n = len(arr)
dp = [1] * n

for i in range(n):
    for j in range(i):
        if arr[i] > arr[j]:
            dp[i] = max(dp[i], dp[j] + 1)

print(max(dp))

```

## Using Js
```
let arr = [10,9,2,5,3,7,101,18];

let n = arr.length;
let dp = new Array(n).fill(1);

for (let i = 0; i < n; i++) {
  for (let j = 0; j < i; j++) {
    if (arr[i] > arr[j]) {
      dp[i] = Math.max(dp[i], dp[j] + 1);
    }
  }
}

console.log(Math.max(...dp));
```
