# Allow One Function Call
# Problem

Given a function fn, return a new function that is identical to the original function except that it ensures fn is called at most once.

The first time the returned function is called, it should return the same result as fn.
Every subsequent time it is called, it should return undefined.

# Solution
## Using Js
```
var once = function (fn) {
  let called = false;
  return function (...args) {
    if (!called) {
      called = true;
      return fn(...args);
    }
    return undefined;
  };
};

const fn = (a, b, c) => a + b + c;
const call = [1, 2, 3];
const onceFn = fn(...call);
console.log(onceFn);

```

## Using Python
```


def once(fn):
    called = False

    def wrapper(*args, **kwargs):
        nonlocal called
        if not called:
            called = True
            return fn(*args, **kwargs)
        return None

    return wrapper      


def fn(a, b, c):
    return a + b + c   
call = [1, 2, 3]
once_fn = once(fn) 
print(once_fn(*call))
```
