# 🧮 Factorial Problem Statement

## Problem:
Given a non-negative integer n, write a function to calculate its factorial.

The factorial of a number n is defined as:
```
n!=n×(n−1)×(n−2)×⋯×1
```
For n = 0, the factorial is defined as:

0! = 1
📥 Input
An integer n where 0 ≤ n ≤ 1000
📤 Output
Return the factorial of n

## Solution
### Using Python :
Method 1: recursion
- time compleixity :O(N)
- space complpexity :O(N) .. satck space

```
def fun(n):
    if n==1:
        return 1

    return n* fun(n-1)

print(fun(5))
```
