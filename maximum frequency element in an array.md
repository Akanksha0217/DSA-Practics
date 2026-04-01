# 🚀 Question
Find the maximum frequency element in an array

# 🧠 Problem
Given an array, find the element that appears most frequently

## Solution 
### Using Python
```
arr = [1, 3, 2, 1, 4, 1, 3]

freq = {}
max_fr = 0
result = None

for num in arr:
    if num in freq:
        freq[num] += 1
    else:
        freq[num] = 1

    if freq[num] > max_fr:
        max_fr = freq[num]
        result = num

print(result)
```

### Using JS
```
let arr = [1, 3, 2, 1, 4, 1, 3];

let has = {};
let max_fr = 0;
let result = 0;
for (let num of arr) {
  if (num in has) {
    has[num] += 1;
  } else {
    has[num] = 1;
  }
  if (has[num] > max_fr) {
    max_fr = has[num];
    result = num;
  }
}
console.log(result);

```
