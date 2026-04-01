
# 🚀 Question
Find the intersection of two arrays

## 🧠 Problem

Given two arrays, return the common elements

## Solution 

### Using Python
 ### Method 1
```
arr1 = [1, 2, 2, 1]
arr2 = [2, 2]
arr3=[]

for num in arr1:
    for n1 in arr2:
        if num == n1:
            if num not in arr3:
                arr3.append(num)

print(arr3)
```
  ### Method 2
 ```
arr1 = [1, 2, 2, 1]
arr2 = [2, 2]

result = list(set(arr1) & set(arr2))

print(result)
```

### Using JS
```
let arr1 = [1, 2, 2, 1];
let arr2 = [2, 2];

let set = new Set();

for (let i = 0; i < arr1.length; i++) {
  for (let j = 0; j < arr2.length; j++) {
    if (arr1[i] == arr2[j]) {
      set.add(arr1[i]); // no need to check has()
    }
  }
}

console.log([...set]);
``
