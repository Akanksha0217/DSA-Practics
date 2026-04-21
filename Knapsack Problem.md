# 🚀 Question

0/1 Knapsack Problem

## 🧠 Problem

You are given:

weights = [1,3,4,5]
values  = [1,4,5,7]
capacity = 7

👉 You can pick items only once (0 or 1)
👉 Maximize total value

✅ Output
9

# Solution
## Using Python 
```
weights = [1,3,4,5]
values = [1,4,5,7]
capacity = 7

n = len(weights)

def knapsack(i, cap):
    if i == n or cap == 0:
        return 0

    # skip
    skip = knapsack(i+1, cap)

    # take (if possible)
    take = 0
    if weights[i] <= cap:
        take = values[i] + knapsack(i+1, cap - weights[i])

    return max(take, skip)

print(knapsack(0, capacity))
```

## Using JS
```
```
