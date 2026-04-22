# 🚀 Question

 Valid Parentheses

## 🧠 Problem

Given a string:

s = "()[]{}"

👉 Check if it is valid

✅ Rules
( must close with )
{ must close with }
[ must close with ]
Order must be correct

# Solution

## Using Python
```
s = "()[]{}"

stack = []

pairs = {
    ')': '(',
    '}': '{',
    ']': '['
}

for ch in s:
    if ch in pairs.values():  # opening
        stack.append(ch)
    else:
        if not stack or stack[-1] != pairs[ch]:
            print(False)
            break
        stack.pop()
else:
    print(len(stack) == 0)
```

## Using JS
```
let s = "()[]{}";

let stack = [];

let pairs = {
  ')': '(',
  '}': '{',
  ']': '['
};

let valid = true;

for (let ch of s) {
  if (Object.values(pairs).includes(ch)) {
    stack.push(ch);
  } else {
    if (stack.length === 0 || stack[stack.length - 1] !== pairs[ch]) {
      valid = false;
      break;
    }
    stack.pop();
  }
}

console.log(valid && stack.length === 0);
```
