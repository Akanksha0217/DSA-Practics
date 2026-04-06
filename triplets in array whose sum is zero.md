# 🚀 Question

Find all triplets in array whose sum = 0 (3Sum Problem)

## 🧠 Problem

Given:
arr = [-1,0,1,2,-1,-4]
Find all triplets:
a + b + c = 0

## Solution
## Using Python
```
arr = [-1,0,1,2,-1,-4]

arr.sort()
n = len(arr)
result = []

for i in range(n):
    if i > 0 and arr[i] == arr[i-1]:
        continue

    left = i + 1
    right = n - 1

    while left < right:
        total = arr[i] + arr[left] + arr[right]

        if total == 0:
            result.append([arr[i], arr[left], arr[right]])
            left += 1
            right -= 1

            while left < right and arr[left] == arr[left-1]:
                left += 1
            while left < right and arr[right] == arr[right+1]:
                right -= 1

        elif total < 0:
            left += 1
        else:
            right -= 1

print(result)
```

## Using JS
```
let arr = [-1,0,1,2,-1,-4];

arr.sort((a,b) => a-b);
let result = [];

for (let i = 0; i < arr.length; i++) {

  if (i > 0 && arr[i] === arr[i-1]) continue;

  let left = i + 1;
  let right = arr.length - 1;

  while (left < right) {
    let sum = arr[i] + arr[left] + arr[right];

    if (sum === 0) {
      result.push([arr[i], arr[left], arr[right]]);

      left++;
      right--;

      while (left < right && arr[left] === arr[left-1]) left++;
      while (left < right && arr[right] === arr[right+1]) right--;

    } else if (sum < 0) {
      left++;
    } else {
      right--;
    }
  }
}

console.log(result);
```



