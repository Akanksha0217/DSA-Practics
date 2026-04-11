# 🚀 Question

Find the Median of Two Sorted Arrays

## 🧠 Problem

Given two sorted arrays:
Find the median

## SOLUTION
# Using Python
```
arr1 = [1,3]
arr2 = [2]

arr = arr1 + arr2
arr.sort()

n = len(arr)

if n % 2 == 1:
    print(arr[n//2])
else:
    print((arr[n//2 - 1] + arr[n//2]) / 2)
```
# Using Js
```
let arr1 = [1,3];
let arr2 = [2];

let arr = arr1.concat(arr2).sort((a,b) => a-b);

let n = arr.length;

if (n % 2 === 1) {
  console.log(arr[Math.floor(n/2)]);
} else {
  console.log((arr[n/2 - 1] + arr[n/2]) / 2);
}
```
