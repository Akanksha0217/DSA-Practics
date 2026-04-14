# 🚀 Question
Find a Peak Element

## 🧠 Problem
Given:
arr = [1,2,3,1]


✅ Output
2  (index of value 3)

 Another Example
arr = [1,2,1,3,5,6,4]
👉 Output can be:
1 (value 2) OR 5 (value 6)
👉 Multiple answers possible ✅

## Solution
### Using Python
```
arr = [1,2,3,1]

left = 0
right = len(arr) - 1

while left < right:
    mid = (left + right) // 2

    if arr[mid] < arr[mid + 1]:
        left = mid + 1
    else:
        right = mid

print(left)  # index of peak
```

### Using JS
```
let arr = [1,2,3,1];

let left = 0;
let right = arr.length - 1;

while (left < right) {
  let mid = Math.floor((left + right) / 2);

  if (arr[mid] < arr[mid + 1]) {
    left = mid + 1;
  } else {
    right = mid;
  }
}

console.log(left);
```
