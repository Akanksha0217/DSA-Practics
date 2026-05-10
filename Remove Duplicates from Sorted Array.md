# Problem
Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. The relative order of the elements should be kept the same.

Consider the number of unique elements in nums to be k​​​​​​​​​​​​​​. After removing duplicates, return the number of unique elements k.

The first k elements of nums should contain the unique numbers in sorted order. The remaining elements beyond index k - 1 can be ignored.

### Example
Input: nums = [0,0,1,1,1,2,2,3,3,4]
Output: 5

## Solution
### Method 1:
- Time :O(2N)
- space :O(N)
-
```
arr=[1,1,2,3,4,4,5,5,6,6,6,7,7,7,10]
n=len(arr)
fer={}
for i in range(n):
    fer[arr[i]]=0
    
j=0

for i in fer:
        arr[j]=i
        j+=1
  
    
print(j)
```

### Method 2:
- Time :O(N)
- space :O(1)
```
arr=[1,1,2,3,4,4,5,5,6,6,6,7,7,7,10]
n=len(arr)
i=0
j=i+1
while j<n:
        if arr[i]!=arr[j]:
            i+=1
            arr[i],arr[j]=arr[j],arr[i]
        j+=1

print(i+1)
```
