# ✅ Longest Substring Without Repeating Characters
## 🧠 Problem Statement
Given a string s, find the length of the longest substring without repeating characters.
A substring means characters must be continuous.

📥 Example 1
Input:  "abcabcbb"
Output: 3

## Solution
### In Python
```
def substring(s):
    maxlength=0

    for i in range(len(s)):
        seen=""
        for j in range(i,len(s)):
            if s[j] in seen:
                break 
            seen +=s[j]
            maxlength=max(maxlength,len(seen))
    return maxlength

print(substring("abcabcbb"))
```
### In JS
```
function longestSubstring(str) {
  let maxLength = 0;

  for (let i = 0; i < str.length; i++) {
    let seen = "";

    for (let j = i; j < str.length; j++) {
      if (seen.includes(str[j])) {
        break;
      }

      seen += str[j];
      maxLength = Math.max(maxLength, seen.length);
    }
  }

  return maxLength;
}
console.log(longestSubstring("abcabcbb"));

```
