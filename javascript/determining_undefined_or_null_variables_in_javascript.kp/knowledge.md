---
title: What is the difference between an 'undefined' and a 'null' variable?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `typeof` operator to check if a variable is undefined or null.
---

**Contents**

[TOC]

# Using the Equality Operator

The equality operator (`==`) can be used to check for both `undefined` and `null` values in Javascript. To check for `undefined`, you can use the following code:

```javascript
if (myVariable == undefined) {
  // Do something
}
```

Similarly, to check for `null`, you can use the following code:

```javascript
if (myVariable == null) {
  // Do something
}
```

# Using the Strict Equality Operator

The strict equality operator (`===`) can also be used to check for both `undefined` and `null` values in Javascript. To check for `undefined`, you can use the following code:

```javascript
if (myVariable === undefined) {
  // Do something
}
```

Similarly, to check for `null`, you can use the following code:

```javascript
if (myVariable === null) {
  // Do something
}
```

# Using the typeof Operator

The `typeof` operator can also be used to check for both `undefined` and `null` values in Javascript. To check for `undefined`, you can use the following code:

```javascript
if (typeof myVariable === 'undefined') {
  // Do something
}
```

Similarly, to check for `null`, you can use the following code:

```javascript
if (myVariable === null) {
  // Do something
}
```
