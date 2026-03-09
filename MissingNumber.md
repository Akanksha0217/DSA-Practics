# 🚀 Question: Find the Missing Number
## 🧠 Problem
You are given numbers from 1 to n, but one number is missing.
Find the missing number.

📥 Example
```
arr = [1,2,4,5]
output:3
```

## solution
### M1 : Python using Numerical formula 
```
def missingNumber(arr):
    n=len(arr)
    sum1=(n+1)*(n+2)//2
    sum2=sum(arr)           
    return sum1-sum2  
  
print(missingNumber([1,2,3,5]))
```

### M2 : Using Set in Python
```
arr = [1,2,4,5]
n = len(arr) + 1
s = set(arr)
for i in range(1, n+1):
    if i not in s:
        print(i)
```

### JS using Numerical formula 
```
function missN(arr) {
  let n = arr.length + 1;
  let sum = (n * (n + 1)) / 2;
  let sum1 = 0;
  for (let num of arr) {
    sum1 += num;
  }
  return sum - sum1;
}
console.log(missN([1, 2, 3, 4, 6]));
```

### Js using Set method
```
let arr = [1, 2, 4, 5];
let n = arr.length + 1;
s = new Set(arr);
console.log(s);

for (let i = 1; i <= n; i++) {
  if (!s.has(i)) {
    console.log(i);
  }
}
```
