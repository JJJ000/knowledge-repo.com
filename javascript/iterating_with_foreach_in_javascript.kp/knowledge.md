---
title: Iterate to the next item in the JavaScript foreach loop
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The next iteration in a JavaScript forEach loop is determined by the function`s callback, which is invoked with each element in the array.
---

**Contents**

[TOC]

# Iterating in a forEach Loop
A forEach loop is a type of loop that can be used to iterate over an array. This loop is typically used to perform an action on each element in the array. The syntax for a forEach loop is as follows:

```
array.forEach(function(element) {
    // Do something with element
});
```

# Moving to the Next Iteration
In order to move to the next iteration in a forEach loop, you can simply use the `continue` statement. This will skip the current iteration and move to the next one. The syntax for this is as follows:

```
array.forEach(function(element) {
    // Do something with element
    continue;
});
```

# Breaking Out of a forEach Loop
In order to break out of a forEach loop, you can use the `break` statement. This will stop the loop from running and exit it. The syntax for this is as follows:

```
array.forEach(function(element) {
    // Do something with element
    break;
});
```
