# 🚀 Question: First Non-Repeating Character in a String
## 🧠 Problem
Find the first character in a string that appears only once.

## Solution
### Method 1:Two Loops 
### Using Python
```
let str = "aabbcdde";

for (let i = 0; i < str.length; i++) {
  let count = 0;

  for (let j = 0; j < str.length; j++) {
    if (str[i] === str[j]) {
      count++;
    }
  }

  if (count === 1) {
    console.log(str[i]);
    break;
  }
}
```
### Using Js

```
let s = "aabbcdd";
let s1 = "";

for (let i = 0; i < s.length; i++) {
  let count = 0;
  for (let j = 0; j < s.length; j++) {
    if (s[i] == s[j]) {
      count += 1;
    }
  }
  if (count == 1) {
    console.log(s[i]);
    break;
  }
}

```

### Method 1:HashMap / Dictionary 
### Using Python

```
s="aabbcdd"

freq = {}

for ch in s:
    if ch in freq:
        freq[ch] += 1
    else:
        freq[ch] = 1

for ch in s:
    if freq[ch] == 1:
        print(ch)
        break
```

### Using JS
```
let s = "aabbcdd";
let s1 = {};

for (let ch of s) {
  if (ch in s1) {
    s1[ch] += 1;
  } else {
    s1[ch] = 1;
  }
}

for (let ch of s) {
  if (s1[ch] == 1) {
    console.log(ch);
    break;
  }
}

```



```
