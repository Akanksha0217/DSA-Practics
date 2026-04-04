# 🚀 Question

Find the container with most water

# 🧠 Problem

You are given heights:

arr = [1,8,6,2,5,4,8,3,7]

Each index = vertical line

👉 Two lines form a container
 
📦 Water Formula
water = min(height[left], height[right]) * (right - left)

# Solution
## Using Python
```
arr = [1, 8, 6, 2, 5, 4, 8, 3, 7]


left = 0
right = len(arr) - 1
water = 0
max_height = 0


while left < right:
    height=min(arr[left],arr[right])
    width=right-left
    water=height*width
    max_height=max(max_height,water)

    if arr[left]<arr[right]:
        left+=1
    else:
        right-=1   

print(max_height)
```

## Using JS
```
arr = [1, 8, 6, 2, 5, 4, 8, 3, 7];

let left = 0;
let right = arr.length - 1;
let water = 0;
let max_height = 0;

while (left < right) {
  let height = Math.min(arr[left], arr[right]);
  let width = right - left;
  water = height * width;
  max_height = Math.max(max_height, water);

  if (arr[left] < arr[right]) {
    left++;
  } else {
    right--;
  }
}

console.log(max_height);

```
