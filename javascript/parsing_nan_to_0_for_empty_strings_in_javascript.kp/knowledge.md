---
title: What is the best way to convert an empty string to 0 when using parseint() to get a nan result?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the ternary operator (?) to check if parseInt returns NaN, and if so, set the value to 0.
---

**Contents**

[TOC]

# Section 1 - Check for Empty String

We can use the `typeof` operator to check if a given value is an empty string.

```
if (typeof myString === 'string' && myString.length === 0) {
  // Empty string
}
```

# Section 2 - Parse the String

We can use the `parseInt` function to convert the string into an integer.

```
var myNumber = parseInt(myString);
```

# Section 3 - Check for NaN

We can use the `isNaN` function to check if the result of `parseInt` is `NaN`.

```
if (isNaN(myNumber)) {
  // NaN
}
```

# Section 4 - Replace NaN with 0

If the result of `parseInt` is `NaN`, we can replace it with `0`.

```
if (isNaN(myNumber)) {
  myNumber = 0;
}
```
