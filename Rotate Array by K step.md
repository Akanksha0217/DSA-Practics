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
### Method 1:
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

### Method 2:
- Time Complexity: O(N)
- space Complexity;O(1)
```
num=[1,2,3,4,5]
k=2
n=len(num)

k=k%n
def reverse(nums,left,right):
    while left<right:
        nums[left],nums[right]=nums[right],nums[left]
        left+=1
        right-=1

reverse(num,n-k,n-1)  
reverse(num,0,n-k-1)
reverse(num,0,n-1)
print(num)
```

