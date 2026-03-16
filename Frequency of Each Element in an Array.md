# 🚀 Question: Find Frequency of Each Element in an Array
## 🧠 Problem
Given an array, count how many times each element appears.

## Solution 
### Using Python
```
arr=[1,2,2,1,1,3,3,3,3]

hash={}
count =0
for i in arr:
    if i in hash:
        hash[i] +=1
    else:
        hash[i] =1

print(hash)
```

## Solution 
### Using JS
```
let arr = [1, 2, 2, 3, 3, 3];

let freq = {};

for (let num of arr) {
  if (num in freq) {
    freq[num] += 1;
  } else {
    freq[num] = 1;
  }
}

console.log(freq);
```
