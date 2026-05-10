# Rotate Array by 1:
🧠 Problem Statement
Given an array , rotate the array to the right by once steps.


## Solution
## Using Python
```
num=[1,2,3,4,5]
n=len(num)
temp=num[n-1]

for i in range(n-2,-1,-1):
    num[i+1]=num[i]
num[0]=temp 
print(num)
```
