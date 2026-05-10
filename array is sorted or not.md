# 🚀 Question

Check if an array is sorted or not

# 🧠 Problem

Given an array, check whether it is:

👉 Sorted in ascending order

## Method 1:
### Using Python
- Time complexity :O(n)
- space complexity :O(1)
```
arr = [1,2,3,5,4]

is_sorted = True

for i in range(len(arr)-1):
    if arr[i] > arr[i+1]:
        is_sorted = False
        break

print(is_sorted)
```

### Using JS
```
let arr = [1, 2, 3, 4, 5];
let is_sorted = true;

for (let i = 0; i < arr.length; i++) {
  if (arr[i] > arr[i - 1]) {
    is_sorted = false;
    break;
  }
}
console.log(is_sorted);

```
## Method 2:
### Using Python
- Time complexity : O(n log n)
- space complexity :O(n)
-
```
arr= [2,1,3,4]
arr_sort = sorted(arr)

if arr==arr_sort:
    print("True")
else:    
    print("False")
```
