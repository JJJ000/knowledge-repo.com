---
title: Creating multiple variables in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Declaring multiple variables in JavaScript can be done by separating each variable with a comma.
---

**Contents**

[TOC]

### Single Line

We can declare multiple variables in a single line in Javascript, separating them with a comma:

```javascript
var x = 5, y = 10, z = 15;
```

### Multiple Lines

We can also declare multiple variables in multiple lines in Javascript, assigning each one its own line:

```javascript
var x = 5;
var y = 10;
var z = 15;
```

### Destructuring

We can also use destructuring to assign multiple variables in a single line in Javascript:

```javascript
var [x, y, z] = [5, 10, 15];
```

### For Loop

We can also use a for loop to declare multiple variables in Javascript:

```javascript
for (var i = 0, x = 5, y = 10, z = 15; i < 3; i++) {
    // Do something
}
```
