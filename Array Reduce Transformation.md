# Array Reduce Transformation

# Problem
nums = [1,2,3,4]
fn = function sum(accum, curr) { return accum + curr; }
init = 0
Output: 10
Explanation:
initially, the value is init=0.
(0) + nums[0] = 1
(1) + nums[1] = 3
(3) + nums[2] = 6
(6) + nums[3] = 10
The final answer is 10.

# Solution
## Using Js
```
var reduce = function (nums, fn, init) {
  let result = init;
  for (let i = 0; i < nums.length; i++) {
    result = fn(result, nums[i]);
  }

  return result;
};

((nums = [1, 2, 3, 4]),
  (fn = function sum(accum, curr) {
    return accum * curr;
  }),
  (init = 1));
console.log(reduce(nums, fn, init));

````

## Using Js
```
def reduce(num,fn,init):
    result=init
    for i in num:
        result=fn(result,i )
    return result

num=[1,2,3,4,5]
def add(x,y):
    return x+y
init=0
print(reduce(num,add,init))

```
