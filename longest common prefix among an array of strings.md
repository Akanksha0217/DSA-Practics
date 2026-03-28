
# 🚀 Question

Find the longest common prefix among an array of strings

# 🧠 Problem

Given an array of strings, find the common starting characters.

## Solution
### USing python
```
arr = ["flower","flow","flight"]

prefix = ""

for i in range(len(arr[0])):   # loop through first string
    
    ch = arr[0][i]

    for word in arr:
        if i >= len(word) or word[i] != ch:
            print(prefix)
            exit()
    
    prefix += ch

print(prefix)
```



### Using Js
```
let arr = ["bflower", "flow", "flight"];

let prefix = "";

for (let i = 0; i < arr[0].length; i++) {
  let ch = arr[0][i];

  for (let word of arr) {
    if (i >= word.length || word[i] !== ch) {
      console.log(prefix);
      return;
    }
  }

  prefix += ch;
}
```
