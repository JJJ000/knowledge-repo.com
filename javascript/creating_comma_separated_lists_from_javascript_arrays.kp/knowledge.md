---
title: How can I create a comma-separated list from a JavaScript array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Array.prototype.join() method to turn an array into a comma-separated list.
---

**Contents**

[TOC]

**Section 1: Create a Function**

Create a function that takes an array as an argument and returns a comma-separated list.

```javascript
function arrayToCommaSeparatedList(arr) {
  let result = '';
  for (let i = 0; i < arr.length; i++) {
    result += arr[i] + ', ';
  }
  return result.slice(0, -2);
}
```

**Section 2: Call the Function**

Call the function with an array of strings as the argument.

```javascript
let array = ["apples", "oranges", "bananas"];
let commaSeparatedList = arrayToCommaSeparatedList(array);
```

**Section 3: Output the Result**

Print the result to the console.

```javascript
console.log(commaSeparatedList);
```

**Section 4: Result**

The output should be a comma-separated list of strings:

`apples, oranges, bananas`
