# 🚀 Question

Find the first missing positive number

## 🧠 Problem
Given an unsorted array, find the smallest missing positive integer.
## Solution

## Using Python
```
arr = [3,4,-1,1,2]

s = set(arr)

i = 1

while True:
    if i not in s:
        print(i)
        break
    i += 1

```

## Using Js
```
let arr = [3, 4, -1, 1, 2];

// let s = new set(arr);
let s = new Set(arr);

let i = 1;
// let valid = true;
while (true) {
  if (!s.has(i)) {
    console.log(i);
    break;
  }
  i++;
}


```
