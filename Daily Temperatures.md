# 🚀 Question

Daily Temperatures
---
 🧠 Problem

Given temperatures:

temps = [73,74,75,71,69,72,76,73]

👉 For each day, find how many days to wait for a warmer temperature

✅ Output
[1,1,4,2,1,1,0,0]
---
# Solution
## Method 1: Using Js 
- Brute Force Approach
- Time Complexity:O(n²) 
- Space Complexity :O(n)
```
let temps = [73, 74, 75, 71, 69, 72, 76, 73];
let result = [];

for (let i = 0; i < temps.length; i++) {
    let count = 0;
    let found = false;

    for (let j = i + 1; j < temps.length; j++) {
        count++;
        if (temps[j] > temps[i]) {
            result.push(count);
            found = true;
            break;
        }
    }

    if (!found) {
        result.push(0);
    }
}

console.log(result);
```
