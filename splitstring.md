# Problem 
in js write function that takes a strings ,splits the string by dots(.) and retuen second last string from that splits .if there are no dots in original string return an empty string.example "ggg.ttt.com" the return "ttt"

# Solution

## Using Js
```
function getSecondLast(str) {
    let parts = str.split('.');

    if (parts.length < 2) {
        return '';
    }

    return parts[parts.length - 2];
}

// Example usage
console.log(getSecondLast("ggg.ttt.com")); // ttt
console.log(getSecondLast("hello")); // ""
```
