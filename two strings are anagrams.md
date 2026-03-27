# 🚀 Question

Check if two strings are anagrams

## 🧠 Problem

Two strings are anagrams if:
👉 They contain the same characters
👉 With the same frequency
👉 Order does NOT matter

## Solution
### Using Python 
```
s1 = "listen"
s2 = "silent"

if sorted(s1) == sorted(s2):
    print(True)
else:
    print(False)
```

### Using JS
```
let s1 = "listen";
let s2 = "silent";

if (s1.split("").sort().join("") === s2.split("").sort().join("")) {
  console.log(true);
} else {
  console.log(false);
}
```
