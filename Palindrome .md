# 🚀 Question: Check if a String is Palindrome
## 🧠 Problem
A palindrome is a word that reads the same forward and backward.

## Solution
## M1:
#### Using Python 
```
s="madam"
reverse=""

for i in s:
    reverse +=i

if reverse == s:
    print("String is  Palindrome")
```
#### Using JS
```
let str = "madam";
let reverse = "";
for (let i = str.length - 1; i >= 0; i--) {
  reverse += str[i];
}
if (reverse == str) {
  console.log("str is palindrome");
}
```

## M2:
### Using Python
```
s = "madam"
is_palindrome = True

for i in range(len(s)//2):
    if s[i] != s[len(s)-1-i]:
        is_palindrome = False
        break

print(is_palindrome)
```

#### Using JS
```
let str = "madam";

let isPalindrome = true;

for (let i = 0; i < str.length / 2; i++) {
  if (str[i] !== str[str.length - 1 - i]) {
    isPalindrome = false;
    break;
  }
}

console.log(isPalindrome);
```

## Method 3
### Using Python
```
n=1234
num=n
result=0
while num>0:
    digit = num % 10
    result = result * 10 + digit
    num = num // 10


if n==result:
    print("Palindrome")
else:    print("Not Palindrome")
```
