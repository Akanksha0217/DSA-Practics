# 🚀 Question

Check if the given string has valid parentheses

## 🧠 Problem
A string is valid if:
1️⃣ Open brackets are closed properly
2️⃣ Order is correct


## SOlution
## Using Python

```
let s = "()[]{}";
let stack = [];
let mapping = {
  ")": "(",
  "}": "{",
  "]": "["
};
let isValid = true;
for (let ch of s) {
  if (["(", "{", "["].includes(ch)) {
    stack.push(ch);
  } else {
    if (stack.length === 0 || stack[stack.length - 1] !== mapping[ch]) {
      isValid = false;
      break;
    }
    stack.pop();
  }
}
if (isValid && stack.length === 0) {
  console.log(true);
} else {
  console.log(false);
}
```

### Using Js
```
s = "()[]{}"

stack = []
mapping = {')': '(', '}': '{', ']': '['}

is_valid = True

for ch in s:
    if ch in mapping.values():  # opening brackets
        stack.append(ch)
    else:  # closing brackets
        if not stack or stack[-1] != mapping[ch]:
            is_valid = False
            break
        stack.pop()

if is_valid and not stack:
    print(True)
else:
    print(False)
```
