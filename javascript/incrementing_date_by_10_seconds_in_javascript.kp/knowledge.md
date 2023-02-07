---
title: Increase a date by 10 seconds
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: date.setSeconds(date.getSeconds() + 10);
---

**Contents**

[TOC]

### Using Date.setSeconds()

```javascript
let currentDate = new Date();
currentDate.setSeconds(currentDate.getSeconds() + 10);
console.log(currentDate);
```

### Using Date.getTime()

```javascript
let currentDate = new Date();
let newTime = currentDate.getTime() + (10 * 1000);
let newDate = new Date(newTime);
console.log(newDate);
```

### Using Date.now()

```javascript
let currentDate = new Date();
let newTime = Date.now() + (10 * 1000);
let newDate = new Date(newTime);
console.log(newDate);
```

### Using Date.prototype.valueOf()

```javascript
let currentDate = new Date();
let newTime = currentDate.valueOf() + (10 * 1000);
let newDate = new Date(newTime);
console.log(newDate);
```
