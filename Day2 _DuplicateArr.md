
### ✅ Find the Duplicate Number in an Array
🧠 Problem Statement
You are given an array of integers where one number appears more than once.
Your task is to find the duplicate number.

## solution:
### M1 :Brute Force Approach. in Python
```
arr=[1,2,3,2,4]

for i in range(len(arr)):
    for j in range(i+1,len(arr)):
        if arr[i]==arr[j]:
            print(arr[i])
         
```

### M2 :Brute Force Approach. in JS
```
let arr = [1, 2, 3, 4, 5, 2];
for (let i = 0; i < arr.length; i++) {
  for (let j = i + 1; j < arr.length; j++) {
    if (arr[i] == arr[j]) {
      console.log(arr[i]);
    }
  }
}
```
### M3: HashMap 
```
def find_duplicate(arr):
    seen = set()

    for num in arr:
        if num in seen:
            return num
        seen.add(num)

print(find_duplicate([1,2,3,2,4]))
```



```
