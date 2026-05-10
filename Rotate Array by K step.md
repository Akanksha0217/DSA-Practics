# Rotate Array by K Steps
## 🧠 Problem Statement
Given an array and a number k, rotate the array to the right by k steps.
📥 Example
```
Input:
arr = [1,2,3,4,5]
k = 2
```

## Solution
### Using Python 
```
def rotate(arr, k):
    n=len(arr)
    k=k%n

    return arr[-k:]+arr[:-k]

print(rotate([1,2,3,4,5], 3))
```

### Using JS
```
function rotateArr(arr, k) {
  let n = arr.length;
  k = k % n;

  return arr.slice(n - k).concat(arr.slice(0, n - k));
}

console.log(rotateArr([1, 2, 3, 4, 5], 3));
```
