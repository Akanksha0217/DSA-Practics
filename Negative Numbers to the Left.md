# Move All Negative Numbers to the Left
## 🧠 Problem Statement
Given an array of integers, move all negative numbers to the left side of the array and positive numbers to the right side.
You do not need to maintain order.
### 📥 Example
```
Input:  [3, -2, 5, -1, 6, -3]
Output: [-2, -1, -3, 3, 5, 6]
 ```

## Solution
### Using Python M1 :
space Complexity:0(n),
Time Complexity:0(n)
```
arr = [3, -2, 5, -1, 6, -3]
negativeArr=[]
positiveArr=[]

for num in arr:   
    if num<0:    
        negativeArr.append(num)        
    if num>0: 
        positiveArr.append(num)

arr2=negativeArr+positiveArr
print(arr2)
```
### Using Python M2 :
space Complexity:0(n), 
Time Complexity:0(1)

```
def move_negative(arr):
    left = 0
    right = len(arr) - 1

    while left <= right:
        if arr[left] < 0:
            left += 1
        elif arr[right] > 0:
            right -= 1
        else:
            arr[left], arr[right] = arr[right], arr[left]

    return arr

print(move_negative([3, -2, 5,-2, -1, 6, -3]))
```
### Using JS M1 :
```
let arr = [3, -2, 5, -1, 6, -3];
let ngativeArr = [];
let postiveArr = [];

for (let num of arr) {
  if (num < 0) {
    ngativeArr.push(num);
  }
  if (num > 0) {
    postiveArr.push(num);
  }
}
let arr2 = ngativeArr + postiveArr;
console.log(arr2);

```

### Using JS M2:
```
let arr = [3, -2, 5, -1, 6, -3];
let left = 0;
let right = arr.length - 1;

while (left <= right) {
  if (arr[left] < 0) {
    left++;
  }
  if (arr[right] > 0) {
    right--;
  }
  (arr[left], (arr[right] = arr[right]), arr[left]);
}
console.log(arr);
```
