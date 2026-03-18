# 🚀 Question

Find the longest consecutive sequence in an array.
👉 The sequence elements must be continuous numbers, not necessarily in order.

Example
arr = [100, 4, 200, 1, 3, 2]
Output: 4

## Solution
### Uisng Python
```
arr = [100, 4, 200, 1, 3, 2, 5, 6]
a=set(arr)
maxLength = 0

for num in a:
    if num-1 not in a:
        current=num
        length=1

    while current+1 in a:
        current=current+1
        length =length+1
    if maxLength< length:
        maxLength=length


print(maxLength)

```

### Uisng JS
```
let arr = [100, 4, 200, 1, 3, 2, 5, 6];

let set = new Set(arr);

let maxLength = 0;

for (let num of set) {
  
  if (!set.has(num - 1)) {
    let current = num;
    let length = 1;

    while (set.has(current + 1)) {
      current++;
      length++;
    }

    if (length > maxLength) {
      maxLength = length;
    }
  }
}

console.log(maxLength);

```
