# 🧠 Problem: Group Anagrams

# Statement:
Given an array of strings strs, group the anagrams together. You can return the answer in any order.

👉 Two strings are anagrams if they contain the same characters with the same frequency.

📥 Example 1:
Input: strs = ["eat","tea","tan","ate","nat","bat"]  
Output: [["eat","tea","ate"],["tan","nat"],["bat"]]

# Solution

## Using Python
```
strs = ["eat","tea","tan","ate","nat","bat"]

mp = {}

for word in strs:
    key = ''.join(sorted(word))

    if key not in mp:
        mp[key] = []

    mp[key].append(word)

print(list(mp.values()))
```

## Using JS
```
let strs = ["eat","tea","tan","ate","nat","bat"];

let map = {};

for (let word of strs) {
  let key = word.split('').sort().join('');

  if (!map[key]) {
    map[key] = [];
  }

  map[key].push(word);
}

console.log(Object.values(map));
```
