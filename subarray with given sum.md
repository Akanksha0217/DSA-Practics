#🚀 Question

Find the subarray with given sum

## 🧠 Problem
Given an array and a target sum, find a continuous subarray whose sum equals the target.

## Solution
### Using Python
```
arr = [1,2,3,7,5]
target = 12

start = 0
current_sum = 0

for end in range(len(arr)):   
    current_sum += arr[end]  

    while current_sum > target:
        current_sum -= arr[start]
        start += 1

    if current_sum == target:
        print(arr[start:end+1])
        break

```



### Using JS
```
let arr = [1, 2, 3, 7, 5];
let target = 12;

let start = 0;
let curr_sum = 0;

for (let i = 0; i < arr.length; i++) {
  curr_sum += arr[i];

  while (curr_sum > target) {
    curr_sum -= arr[start];
    start++;
  }
  if (curr_sum == target) {
    console.log(arr.slice(start, i + 1));
    break;
  }
}

```
