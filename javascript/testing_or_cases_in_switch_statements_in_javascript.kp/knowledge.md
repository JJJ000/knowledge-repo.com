---
title: Check for multiple conditions within a switch statement, similar to using an or operator (||)
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the `fallthrough` keyword to test for multiple cases in a switch statement.
---

**Contents**

[TOC]

**Section 1: Using fall-through**

Switch statements in many languages, including JavaScript, allow for the use of fall-through. This means that when a specific case is met, the code in that case and all of the cases below it will be executed. This allows for the use of multiple cases in a switch statement. For example:

```
switch (x) {
  case 1:
  case 2:
  case 3:
    // code to be executed when x is 1, 2, or 3
    break;
  case 4:
    // code to be executed when x is 4
    break;
  default:
    // code to be executed when x is not 1, 2, 3, or 4
    break;
}
```

In this example, when `x` is 1, 2, or 3, the code in the first block will be executed.

**Section 2: Using multiple cases**

It is also possible to use multiple cases in a switch statement without using fall-through. In this case, each case must be listed explicitly and the `break` statement must be used after each case. For example:

```
switch (x) {
  case 1:
  case 2:
    // code to be executed when x is 1 or 2
    break;
  case 3:
  case 4:
    // code to be executed when x is 3 or 4
    break;
  default:
    // code to be executed when x is not 1, 2, 3, or 4
    break;
}
```

In this example, when `x` is 1 or 2, the code in the first block will be executed, and when `x` is 3 or 4, the code in the second block will be executed.

**Section 3: Using logical OR (||)**

It is also possible to use a logical OR (||) operator in a switch statement. This allows for multiple cases to be evaluated in a single case statement. For example:

```
switch (x) {
  case 1 || 2:
    // code to be executed when x is 1 or 2
    break;
  case 3 || 4:
    // code to be executed when x is 3 or 4
    break;
  default:
    // code to be executed when x is not 1, 2, 3, or 4
    break;
}
```

In this example, when `x` is 1 or 2, the code in the first block will be executed, and when `x` is 3 or 4, the code in the second block will be executed.

**Section 4: Using multiple switch statements**

It is also possible to use multiple switch statements to test for multiple cases. This allows for a more readable and maintainable code. For example:

```
switch (x) {
  case 1:
    // code to be executed when x is 1
    break;
  case 2:
    // code to be executed when x is 2
    break;
  default:
    // code to be executed when x is not 1 or 2
    break;
}

switch (x) {
  case 3:
    // code to be executed when x is 3
    break;
  case 4:
    // code to be executed when x is 4
    break;
  default:
    // code to be executed when x is not 3 or 4
    break;
}
```

In this example, when `x` is 1, the code in the first block will be executed, and when `x` is 3, the code in the second block will be executed.
