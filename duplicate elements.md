# 🚀 Question
Find all duplicate elements in an array

## 🧠 Problem

Given an array, return all elements that appear more than once.

## Solution

### Using Python
```
arr = [1,2,3,2,4,1]

seen = set()
duplicate = set()

for num in arr:
    if num in seen:
        duplicate.add(num)
    else:
        seen.add(num)

print(list(duplicate))
```

### Using Js
```
let arr = [1,2,3,2,4,1];

let seen = new Set();
let duplicate = new Set();

for (let num of arr) {
  if (seen.has(num)) {
    duplicate.add(num);
  } else {
    seen.add(num);
  }
}

console.log([...duplicate]);
```
