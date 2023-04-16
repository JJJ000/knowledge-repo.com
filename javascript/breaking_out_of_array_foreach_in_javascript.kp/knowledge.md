---
title: Interrupt the execution of array.foreach as if a 'break' statement had been called
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, it is not possible to short circuit Array.forEach like calling break in Javascript.
---

**Contents**

[TOC]

# Solution 1

Create a Custom Loop

The easiest way to short circuit an Array.forEach loop is to create a custom loop. This can be done by using a for loop and implementing a break statement.

```
for (let i = 0; i < arr.length; i++) {
  // Do something
  if (someCondition) {
    break;
  }
}
```

# Solution 2

Use Array.some()

Another way to short circuit an Array.forEach loop is to use Array.some(). This method will iterate through the array until a condition is met, and then it will return true.

```
arr.some(item => {
  // Do something
  return someCondition;
});
```
