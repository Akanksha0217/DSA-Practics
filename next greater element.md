# 🚀 Question
Find the next greater element for each element in an array.

## 🧠 Problem

For every element, find the next element to its right which is greater than it.

If none exists → return -1.

## Solution
### Using Python
```
a = [4, 5, 2, 10]
max = []

for i in range(len(a)):
    found=False
    for j in range(i+1,len(a)):
        if a[i]<a[j]:
            found=True
            max.append(a[j])
            break
    if not found:
        max.append(-1)

print(max)
    
```
### Using JS
```
let a = [4, 5, 2, 10];
let max = [];

for (let i = 0; i < a.length; i++) {
  let found = false;
  for (let j = i + 1; j < a.length; j++) {
    if (a[i] < a[j]) {
      max.push(a[j]);
      found = true;
      break;
    }
  }
  if (!found) {
    max.push(-1);
  }
}

console.log(max);

```
