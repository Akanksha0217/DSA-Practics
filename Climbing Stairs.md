# 🚀 Question

Climbing Stairs

# 🧠 Problem

👉 You are climbing stairs

n = 5

👉 You can take:

1 step
2 steps

👉 How many ways to reach the top?

# Solution
## Using Python
```
n = 5

if n <= 2:
    print(n)
else:
    a, b = 1, 2
    for i in range(3, n + 1):
        a, b = b, a + b
    print(b)
```

## Using JS
```
let n = 5;

if (n <= 2) {
  console.log(n);
} else {
  let a = 1, b = 2;

  for (let i = 3; i <= n; i++) {
    let temp = a + b;
    a = b;
    b = temp;
  }

  console.log(b);
}
```
