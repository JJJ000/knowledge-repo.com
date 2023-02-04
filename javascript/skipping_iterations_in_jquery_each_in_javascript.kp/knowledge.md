---
title: What is the best way to move on to the next iteration in the jquery.each() function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `return false` statement to skip to the next iteration in jQuery.each().
---

**Contents**

[TOC]

**Answer:**

**Using break:**

The `break` statement can be used to skip to the next iteration of the loop. This means that the code after the `break` statement will not be executed.

For example:

```javascript
$.each(array, function(index, value) {
  if (index == 3) {
    break;
  }
  // code that will not be executed if index == 3
});
```

**Using return false:**

The `return false` statement can also be used to skip to the next iteration of the loop. This means that the code after the `return false` statement will not be executed.

For example:

```javascript
$.each(array, function(index, value) {
  if (index == 3) {
    return false;
  }
  // code that will not be executed if index == 3
});
```

**Using continue:**

The `continue` statement can also be used to skip to the next iteration of the loop. This means that the code after the `continue` statement will not be executed.

For example:

```javascript
$.each(array, function(index, value) {
  if (index == 3) {
    continue;
  }
  // code that will not be executed if index == 3
});
```

**Using a flag:**

The `flag` statement can also be used to skip to the next iteration of the loop. This means that the code after the `flag` statement will not be executed.

For example:

```javascript
var flag = false;
$.each(array, function(index, value) {
  if (index == 3) {
    flag = true;
  }
  if (flag) {
    return;
  }
  // code that will not be executed if index == 3
});
```
