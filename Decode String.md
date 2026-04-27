# 🚀 Question
Decode String

## 🧠 Problem

Given:
s = "3[a2[c]]"

👉 Decode the string

✅ Output
"accaccacc"


## Solution
### Using Python
```
s = "3[a2[c]]"

stack = []
current_num = 0
current_str = ""

for ch in s:
    if ch.isdigit():
        current_num = current_num * 10 + int(ch)

    elif ch == "[":
        stack.append((current_str, current_num))
        current_str = ""
        current_num = 0

    elif ch == "]":
        prev_str, num = stack.pop()
        current_str = prev_str + current_str * num

    else:
        current_str += ch

print(current_str)
```

### Using JS
```
let s = "3[a2[c]]";

let stack = [];
let currentNum = 0;
let currentStr = "";

for (let ch of s) {
  if (!isNaN(ch)) {
    currentNum = currentNum * 10 + Number(ch);
  } 
  else if (ch === "[") {
    stack.push([currentStr, currentNum]);
    currentStr = "";
    currentNum = 0;
  } 
  else if (ch === "]") {
    let [prevStr, num] = stack.pop();
    currentStr = prevStr + currentStr.repeat(num);
  } 
  else {
    currentStr += ch;
  }
}

console.log(currentStr);
```
