# 🚀 Question
Find the minimum window substring

## 🧠 Problem

Given two strings:
👉 s (main string)
👉 t (target string)

Find the smallest substring in s that contains all characters of t

## Solution

## Using Python
```
s = "ADOBECODEBANC"
t = "ABC"

min_len = float('inf')
result = ""

for i in range(len(s)):
    for j in range(i, len(s)):
        
        sub = s[i:j+1]

        # check all characters present
        if all(ch in sub for ch in t):
            
            if len(sub) < min_len:
                min_len = len(sub)
                result = sub

print(result)
```

## Using JS
```
let s = "ADOBECODEBANC";
let t = "ABC";

let minLen = Infinity;
let result = "";

for (let i = 0; i < s.length; i++) {
  for (let j = i; j < s.length; j++) {

    let sub = s.substring(i, j + 1);

    // check all characters of t are present
    let valid = true;

    for (let ch of t) {
      if (!sub.includes(ch)) {
        valid = false;
        break;
      }
    }

    if (valid) {
      if (sub.length < minLen) {
        minLen = sub.length;
        result = sub;
      }
    }
  }
}

console.log(result);
```

