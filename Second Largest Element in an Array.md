# 🚀 Question: Second Largest Element in an Array

## 🧠 Problem
Find the second largest number in the array.

## solution 
## method 1:
#### Using python
- time complexity :O(2N)
- space complexity : O(1)
```
nums = [3,2,1,5,6,4]
largest = nums[0]
second_largest = nums[0]
for i in range(len(nums)-1):
    if nums[i] > largest:
        largest = nums[i]

for i in range(len(nums)-1):
    if nums[i]>second_largest and nums[i] != largest:
        second_largest = nums[i]
print(second_largest)


```

## method 2:optimal solution
#### Using python 
- time complexity :O(N)
- space complexity : O(1)
```
nums = [3,2,1,5,6,4]
largest = float('-inf')
second_largest  = float('-inf')
for i in range(len(nums)):
   if nums[i]>largest:
       second_largest = largest
       largest = nums[i]
   elif nums[i]>second_largest and nums[i] != largest:
       second_largest = nums[i]
print(second_largest)

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
