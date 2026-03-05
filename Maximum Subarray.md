# ✅ Maximum Subarray (Kadane’s Algorithm)
## 🧠 Problem Statement
Given an integer array, find the contiguous subarray (subarray elements must be together) that has the largest sum, and return that sum.
Input:  [-2,1,-3,4,-1,2,1,-5,4]
Output: 6

## Solution 
### In Python
```
Input = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
current_sum=0
max_sum=0

for num in Input:
    current_sum+=num
    if current_sum>max_sum:
        max_sum=current_sum
    if current_sum<0:
        current_sum=0

print(max_sum)

```
## In Js
```
let Input = [-2, 1, -3, 4, -1, 2, 1, -5, 4];
let currentSum = 0;
let maxSum = Input[0];
for (let num of Input) {
  currentSum += num;

  if (currentSum > maxSum) {
    maxSum = currentSum;
  }
  if (currentSum < 0) {
    currentSum = 0;
  }
}
console.log(maxSum);

```
