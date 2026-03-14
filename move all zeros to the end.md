
# 🧠 Problem
You are given an array with some zeros and non-zeros.
You need to move all zeros to the end, while keeping the order of non-zero elements unchanged.


# Solution
## Method 1:
### Using Python

```
arr= [1, 2, 0, 0, 3, 0, 4,5]
count =0  

for i in range(0,len(arr)):
    if arr[i] !=0:
        arr[count]=arr[i]
        count += 1
    
while count<len(arr):
    arr[count]==0
    count+=1

print(arr)
    
```

### Using Js
```
let arr = [1, 2, 0, 0, 3, 0, 4];
let count = 0; 

// Move all non-zero elements to the front
for (let i = 0; i < arr.length; i++) {
  if (arr[i] !== 0) {
    arr[count] = arr[i];
    count++;
  }
}
while (count < arr.length) {
  arr[count] = 0;
  count++;
}

console.log(arr);
```

## Method 2:

```
### Using Js
```
let arr = [1, 2, 0, 0, 3, 0, 4];

let arr1 = [];
let arr2 = [];

for (let i = 0; i < arr.length; i++) {
  if (arr[i] !== 0) {
    arr1.push(arr[i]);
  }
  if (arr[i] == 0) {
    arr2.push(arr[i]);
  }
}

console.log(arr1.concat(arr2));

```
