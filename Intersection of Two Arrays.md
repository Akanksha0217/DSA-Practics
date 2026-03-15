# 🚀 Question: Find the Intersection of Two Arrays
## 🧠 Problem
Given two arrays, find the elements that exist in both arrays.

## SOlution
## Using Python
```
arr1 = [1, 2, 3, 4]
arr2 = [3, 4, 5, 6]
result = []

for nu in arr1:
    for n in arr2:
        if nu ==n:
            result.append(nu)

print(result)
```

## Using JS
```
let arr1 = [1, 2, 3, 4];
let arr2 = [3, 4, 5, 6];
let result = [];

for (let i = 0; i < arr1.length; i++) {
  for (let j = 0; j < arr2.length; j++) {
    if (arr1[i] == arr2[j]) {
      result.push(arr1[i]);
    }
  }
}
console.log(result);

```
