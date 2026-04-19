# 🚀 Question

House Robber
## 🧠 Problem
Given houses:
arr = [2,7,9,3,1]

👉 Each number = money in house
👉 You cannot rob adjacent houses
🎯 Goal
👉 Max money you can rob

✅ Output
12
👉 Explanation:
2 + 9 + 1 = 12 ✅

## Solution
### Using Python
```
arr = [2,7,9,3,1]
if len(arr) == 1:
    print(arr[0])
else:
    dp = [0] * len(arr)

    dp[0] = arr[0]
    dp[1] = max(arr[0], arr[1])

    for i in range(2, len(arr)):
        dp[i] = max(dp[i-1], arr[i] + dp[i-2])
    print(dp[-1])
```

### Using JS
```
let arr = [2,7,9,3,1];

if (arr.length === 1) {
  console.log(arr[0]);
} else {
  let dp = new Array(arr.length);

  dp[0] = arr[0];
  dp[1] = Math.max(arr[0], arr[1]);

  for (let i = 2; i < arr.length; i++) {
    dp[i] = Math.max(dp[i-1], arr[i] + dp[i-2]);
  }

  console.log(dp[arr.length - 1]);
}
```
