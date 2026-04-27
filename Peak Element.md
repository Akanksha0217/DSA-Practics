# 🚀 Question

Find Peak Element

## 🧠 Problem

Given:

arr = [1,2,3,1]

👉 Find index of a peak element

### 🧠 What is Peak?

👉 Element greater than its neighbors

3 > 2 and 3 > 1 → peak
✅ Output
2   (index of 3)

## Using Python
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

print(left)
```

## Using Js
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
