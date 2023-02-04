---
title: What is the process for copying a date object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To clone a Date object in Javascript, use the Date.parse() method.
---

**Contents**

[TOC]

### Using the Date Constructor

The easiest way to clone a Date object is to use the Date constructor. This method creates a new Date object with the same properties as the original.

```js
let originalDate = new Date();
let clonedDate = new Date(originalDate);
```

### Using the Date.prototype.getTime() Method

Another way to clone a Date object is to use the Date.prototype.getTime() method. This method returns the number of milliseconds since January 1, 1970, 00:00:00 UTC. This can then be used to create a new Date object.

```js
let originalDate = new Date();
let clonedDate = new Date(originalDate.getTime());
```

### Using the Date.prototype.toISOString() Method

The Date.prototype.toISOString() method can also be used to clone a Date object. This method returns a string in ISO format (yyyy-mm-ddThh:mm:ss.sssZ) which can then be used to create a new Date object.

```js
let originalDate = new Date();
let clonedDate = new Date(originalDate.toISOString());
```

### Using the Date.prototype.toJSON() Method

The Date.prototype.toJSON() method can also be used to clone a Date object. This method returns a string in JSON format (yyyy-mm-ddThh:mm:ss.sssZ) which can then be used to create a new Date object.

```js
let originalDate = new Date();
let clonedDate = new Date(originalDate.toJSON());
```
