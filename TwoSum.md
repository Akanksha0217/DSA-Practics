# ✅ Two Sum Problem
🧠 Problem Statement

Given an array of integers and a target value,
return the indices of two numbers such that they add up to the target.

You cannot use the same element twice.

## solution: 
### Using Python:
```
arr=[10,20,30,40,50]
target=70
for i in range(len(arr)):
    for j in range(i+1,len(arr)):
        if(arr[i]+arr[j]==target):
            print(i,j)
```
### USing Hash method in Python
def two_sum(arr, target):
    hashmap = {}
    result=[]

    for i in range(len(arr)):
        needed = target - arr[i]

        if needed in hashmap:
            result.append([hashmap[needed], i])
          
    
        hashmap[arr[i]] = i

    return result

print(two_sum([2,7,11,15,4,5], 9))

### Using JS
```
let arr=[1,2,3,4,5]
let target=7

for(let i=0;i<arr.length;i++){
    for(let j=i+1;j<arr.length;j++){
        if(arr[i]+arr[j]==target){
            console.log(i,j)
        }
    }
}
```
