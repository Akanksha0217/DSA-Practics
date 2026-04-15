# 🚀 Question

Find the Kth Largest Element

## 🧠 Problem

Given:
arr = [3,2,1,5,6,4]
k = 2
👉 Find the 2nd largest element
✅ Output
5

## Solution
### Method 1
#### Using Python
```
arr = [3,2,1,5,6,4]
k = 2

arr.sort()
print(arr[-k])
````


#### Using Js
```
let arr = [3,2,1,5,6,4];
let k = 2;

arr.sort((a,b) => a-b);
console.log(arr[arr.length - k]);
````
