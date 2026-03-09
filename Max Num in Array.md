# 🚀 Question: Find the Maximum Element in an Array
## 🧠 Problem
Find the largest number in the array.

## Solution 
 ## M1 
 ### Using Python 
```
arr=[1,2,3,4,6,7,1,9]
max_num=arr[0]

for num in arr:
    if num>max_num:
        max_num=num

print("max number in arr is :",max_num)  
```

### Using Js
```
let arr = [1, 2, 3, 4, 5];

let max_num = arr[0];
for (let num of arr) {
  if (num > max_num) {
    max_num = num;
  }
```

## M2 :Sorting
###  using Python
```
arr = [3,7,2,9,5]

arr.sort()

print(arr[-1])
}
console.log("max number in arr is :", max_num);
```
### using Js
```
 let arr = [1, 2, 3, 4, 5];
arr.sort((a,b)=> a-b)
console.log(arr[arr.length-1])
```
