---
title: Is it possible to use parameters with computed properties in vue.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, you can pass parameters to computed properties in Vue.js.
---

**Contents**

[TOC]

### Yes

Computed properties in Vue.js can accept parameters. To do this, you must use a method instead of a property. The method must have a parameter that can be used to calculate the return value of the method.

### Syntax

The syntax for passing a parameter to a computed property is very similar to calling a method. The parameter is passed after the method name, separated by a comma.

```
computed: {
  myComputedProperty (param) {
    // Do something with param
    return result;
  }
}
```

### Example

For example, you can create a computed property that takes a number as a parameter and returns the squared value of that number.

```
computed: {
  squared (num) {
    return num * num;
  }
}
```

### Usage

You can then use the computed property in your template like this:

```
<div>{{ squared(5) }}</div>
```

The result will be 25.
