---
title: An example of using closures in a JavaScript loop
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: A closure inside a loop allows a function to access the loop`s variables from outside the loop.
---

**Contents**

[TOC]

### What is a JavaScript Closure?
A JavaScript closure is a function that has access to its outer lexical environment, even when it is executed outside of its lexical scope. This means that a closure can remember the variables and functions that were available in the scope in which it was created.

### Closures and Loops
A closure can be used inside of a loop to create a function that remembers the value of the loop variable at the time it was created. This can be useful when the loop variable is needed later, after the loop has been completed.

### Example
For example, consider the following loop:

```javascript
for (var i = 0; i < 5; i++) {
  setTimeout(function() {
    console.log(i);
  }, 1000);
}
```

This loop will print out the number 5 five times, because the value of `i` is 5 when the loop has finished executing. To fix this, we can use a closure:

```javascript
for (var i = 0; i < 5; i++) {
  (function(i) {
    setTimeout(function() {
      console.log(i);
    }, 1000);
  })(i);
}
```

### Explanation
In this example, we are creating an anonymous function inside the loop and immediately invoking it with the current value of `i`. This creates a closure that remembers the value of `i` at the time the function was created. When the `setTimeout` callback is executed, it will print out the correct value of `i`.
