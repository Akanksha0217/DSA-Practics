# 🚀 Question: Remove Duplicates from an Array
## 🧠 Problem
Given an array, remove duplicate elements and return only unique elements.

## Solution

### Using Python
```
arr= [1, 2, 2,3,3, 5,5, 4,5]
arr1=[]

for no in arr:
    if no not in arr1:
        arr1.append(no)
           

print(arr1)
    
```

### Using JS
```
let arr = [1, 2, 2, 3, 3, 5, 5, 4, 5];

let arr1 = [];

for (let i of arr) {
  if (!arr1.includes(i)) {
    arr1.push(i);
  }
}

console.log(arr1);

```
