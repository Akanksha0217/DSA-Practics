# 🚀 Question

Merge Overlapping Intervals

# 🧠 Problem

Given intervals:

intervals = [[1,3],[2,6],[8,10],[15,18]]

👉 Merge overlapping intervals

✅ Output
[[1,6],[8,10],[15,18]]

# Solution
## Using Python
```
intervals = [[1,3],[2,6],[8,10]]

intervals.sort()
result = [intervals[0]]

for i in range(1, len(intervals)):
    last = result[-1]
    current = intervals[i]

    if current[0] <= last[1]:
        last[1] = max(last[1], current[1])
    else:
        result.append(current)

print(result)
```

## Using Js
```
let intervals = [[1,3],[2,6],[8,10]];

// Step 1: sort by start
intervals.sort((a, b) => a[0] - b[0]);

let result = [];
result.push(intervals[0]); // first interval

for (let i = 1; i < intervals.length; i++) {
  let last = result[result.length - 1];
  let current = intervals[i];

  // check overlap
  if (current[0] <= last[1]) {
    // merge
    last[1] = Math.max(last[1], current[1]);
  } else {
    // no overlap
    result.push(current);
  }
}
console.log(result);

```

