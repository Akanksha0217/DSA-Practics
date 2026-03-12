# 🚀 Question: Reverse Words in a String
## 🧠 Problem
Reverse the order of words in a sentence.

Example:

Input:  "I love coding"
Output:  "coding love I"

## Solution 
### method 1: Build in Function
#### Using Python
```
s='i love coding'
s1= s.split()
s1.reverse()
result = " ".join(s1)
print(result)
```

#### Using JS
```
let str = "I love coding";
let words = str.split(" ");
words.reverse();
let result = words.join(" ");
console.log(result);
```

### method 2: 
#### Using Python
```
s = "I love coding"
result = ""
word = ""

for i in range(len(s)-1, -1, -1):
    
    if s[i] != " ":
        word = s[i] + word
    
    else:
        result += word + " "
        word = ""

result += word

print(result)
```

#### Using JS
```
let str = "I love coding";

let result = "";
let word = "";

for (let i = str.length - 1; i >= 0; i--) {

  if (str[i] !== " ") {
    word = str[i] + word;
  } else {
    result += word + " ";
    word = "";
  }

}

result += word;

console.log(result);
```
