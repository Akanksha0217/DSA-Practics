# 🚀 Question

Course Schedule

# 🧠 Problem

You have courses:

numCourses = 2
prerequisites = [[1,0]]

Meaning:

To take course 1, first complete course 0
👉 Check if you can finish all courses.
✅ Output
True

Because:
Take 0 → then 1
Possible ✅

## Solution
### Using Python
```
numCourses = 2
prerequisites = [[1,0]]

graph = {i: [] for i in range(numCourses)}

for course, pre in prerequisites:
    graph[course].append(pre)

visiting = set()
visited = set()

def dfs(course):
    if course in visiting:
        return False

    if course in visited:
        return True

    visiting.add(course)

    for pre in graph[course]:
        if not dfs(pre):
            return False

    visiting.remove(course)
    visited.add(course)

    return True

for course in range(numCourses):
    if not dfs(course):
        print(False)
        break
else:
    print(True)
```
### Using Js
```
let numCourses = 2;
let prerequisites = [[1,0]];

let graph = {};

for (let i = 0; i < numCourses; i++) {
  graph[i] = [];
}

for (let [course, pre] of prerequisites) {
  graph[course].push(pre);
}

let visiting = new Set();
let visited = new Set();

function dfs(course) {
  if (visiting.has(course)) return false;
  if (visited.has(course)) return true;

  visiting.add(course);

  for (let pre of graph[course]) {
    if (!dfs(pre)) return false;
  }

  visiting.delete(course);
  visited.add(course);

  return true;
}

let result = true;

for (let i = 0; i < numCourses; i++) {
  if (!dfs(i)) {
    result = false;
    break;
  }
}

console.log(result);

```
