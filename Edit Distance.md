# 🚀 Question

Edit Distance (Levenshtein Distance)

## 🧠 Problem

Given two strings:

word1 = "horse"
word2 = "ros"

👉 Convert word1 → word2 using minimum operations

🔧 Allowed Operations
1. Insert  
2. Delete  
3. Replace

✅ Output
3

🧠 How?
horse → rorse  (replace h → r)
rorse → rose   (delete r)
rose → ros     (delete e)

👉 Total = 3 steps ✅

## Solution
### Using Python
```
word1 = "horse"
word2 = "ros"

n = len(word1)
m = len(word2)

dp = [[0]*(m+1) for _ in range(n+1)]

for i in range(n+1):
    dp[i][0] = i

for j in range(m+1):
    dp[0][j] = j

for i in range(1, n+1):
    for j in range(1, m+1):
        if word1[i-1] == word2[j-1]:
            dp[i][j] = dp[i-1][j-1]
        else:
            dp[i][j] = 1 + min(
                dp[i][j-1],   # insert
                dp[i-1][j],   # delete
                dp[i-1][j-1]  # replace
            )

print(dp[n][m])
```

### Using Js
```
let word1 = "horse";
let word2 = "ros";

let n = word1.length;
let m = word2.length;

let dp = Array.from({length: n+1}, () => new Array(m+1).fill(0));

for (let i = 0; i <= n; i++) dp[i][0] = i;
for (let j = 0; j <= m; j++) dp[0][j] = j;

for (let i = 1; i <= n; i++) {
  for (let j = 1; j <= m; j++) {
    if (word1[i-1] === word2[j-1]) {
      dp[i][j] = dp[i-1][j-1];
    } else {
      dp[i][j] = 1 + Math.min(
        dp[i][j-1],   // insert
        dp[i-1][j],   // delete
        dp[i-1][j-1]  // replace
      );
    }
  }
}
console.log(dp[n][m]);
```
