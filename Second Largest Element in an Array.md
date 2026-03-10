# 🚀 Question: Second Largest Element in an Array

## 🧠 Problem
Find the second largest number in the array.

## solution 
## method 1:
#### Using python 
```
arr=[1,2,3,4,6,7,1,9]
max_num=arr[0]
second=0

for num in arr:
    if num>max_num:
        second= max_num
        max_num=num
    if num>second and num <max_num:
        second=num


print("max number in arr is :",max_num)  
print("second number in arr is :",second)  
```

#### Using JS
```
let arr = [11, 21, 42, 13, 4, 5, 9];
let largest = arr[0]; 
let second = 0;
let temp = 0; 

for (let i = 0; i < arr.length; i++) {
  if (arr[i] > largest) {
    second = largest; //11
    largest = arr[i];
  }
  if (arr[i] > second && arr[i] < largest) {
    second = arr[i];
  }
}
console.log("largest", largest);
console.log("second", second);
```

## method 2: build in function
#### Using python 
```
arr=[1,2,3,4,6,7,1,9]
arr.sort()
print("Second largest number is:",arr[-2])
```

#### Using JS
```
let arr = [11, 21, 42, 13, 4, 5, 9];
arr.sort((a, b) => a - b);

console.log("Second largest number is:", arr[arr.length - 2]);

```
