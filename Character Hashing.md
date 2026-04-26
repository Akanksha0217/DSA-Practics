# Character Hashing

# 🧠 ✅ Problem: Count Frequency of Characters
📌 Problem Statement

You are given a string s and other string q ,you are .

👉 Your task is to finding tha character in q who mang time come in s

# Solution
## Using Python
- Time complexity:O(n+m)
- Space Complexity :O(1)
```
s="abcdxaayzw"
q=["d","x","a","z"]

hash_list=[0]*26
for ch in s:
    ascii_value=ord(ch)
    index=ascii_value-97
    hash_list[index] +=1

for ch in q:
    ascii_value=ord(ch)
    index=ascii_value-97
    print(hash_list[index])

```



## Using Js
```
let s = "abcdxaayzw";
let q = ["d", "x", "a", "z"];

// create array of size 26 filled with 0
let hash_list = new Array(26).fill(0);
for (let ch of s) {
  let index = ch.charCodeAt(0) - 97; 
  hash_list[index] += 1;
}

for (let ch of q) {
  let index = ch.charCodeAt(0) - 97;
  console.log(hash_list[index]);
}

```
