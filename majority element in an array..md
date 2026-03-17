# Find the majority element in an array.
👉 A majority element is the element that appears more than n/2 times.


# Solution
## Method :1
### Using Python
```
arr = [2, 2, 1, 2, 3, 2, 2]
hash = {}
n = len(arr)

for num in arr:
    if num in hash:
        hash[num]+=1
    else:
        hash[num]=1
    if hash[num]>n/2:
        print(num)
        break
```


### Using JS
```
let arr = [2, 2, 1, 2, 3, 2, 2];
let hash = {};
let n = arr.length;
for (let num of arr) {
  if (num in hash) {
    hash[num] += 1;
  } else {
    hash[num] = 1;
  }
  if (hash[num] > n / 2) {
    console.log(num);
    break;
  }
}

```
