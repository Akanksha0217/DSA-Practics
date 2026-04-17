# 🚀 Question 
Coin Change Problem

🧠 Problem

Given:

coins = [1,2,5]
amount = 11

👉 Find minimum number of coins to make amount

✅ Output
3

👉 Because:

5 + 5 + 1 = 11

# Solution
## Using Python
```
coins = [1,2,5]
amount = 11

dp = [float('inf')] * (amount + 1)
dp[0] = 0

for i in range(1, amount + 1):
    for coin in coins:
        if i - coin >= 0:
            dp[i] = min(dp[i], dp[i - coin] + 1)

print(dp[amount] if dp[amount] != float('inf') else -1)
```

## Using Js
```
let coins = [1,2,5];
let amount = 11;

let dp = new Array(amount + 1).fill(Infinity);
dp[0] = 0;

for (let i = 1; i <= amount; i++) {
  for (let coin of coins) {
    if (i - coin >= 0) {
      dp[i] = Math.min(dp[i], dp[i - coin] + 1);
    }
  }
}

console.log(dp[amount] === Infinity ? -1 : dp[amount]);
```
