# 🚀 Question

Find the Next Permutation

# 🧠 Problem
Given an array:
arr = [1,2,3]

# Solution
## Using JS
```
let arr = [1, 2, 3];
let i = arr.length - 2;
// Step 1: find breakpoint
while (i >= 0 && arr[i] >= arr[i + 1]) {
  i--;
}
if (i >= 0) {
  let j = arr.length - 1;
  // Step 2: find just bigger
  while (arr[j] <= arr[i]) {
    j--;
  }
  // Step 3: swap
  [arr[i], arr[j]] = [arr[j], arr[i]];
}
// Step 4: reverse right part
let left = i + 1;
let right = arr.length - 1;

while (left < right) {
  [arr[left], arr[right]] = [arr[right], arr[left]];
  left++;
  right--;
}
console.log(arr);
```

