---
title: A JavaScript switch statement for handling multiple cases
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A switch statement can be used in JavaScript to execute different code for different cases.
---

**Contents**

[TOC]

#### Syntax

```javascript
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

#### Example

```javascript
const month = 2;

switch (month) {
  case 1:
    console.log("January");
    break;
  case 2:
    console.log("February");
    break;
  case 3:
    console.log("March");
    break;
  default:
    console.log("Invalid month");
}

// Output: February
```

#### Explanation

In the above example, the variable `month` is set to `2`. The `switch` statement then checks if `month` is equal to `1`, `2`, or `3`. If `month` is equal to `2`, the code block associated with `case 2` is executed and `"February"` is logged to the console. If `month` is not equal to any of the cases, the code block associated with `default` is executed and `"Invalid month"` is logged to the console.
