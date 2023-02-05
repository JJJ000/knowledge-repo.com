---
title: What is the syntax to display the month and date in JavaScript in two-digit format?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the .toLocaleString() method with the `en-us` locale and the `2-digit` option to get the month and date in 2 digit format.
---

**Contents**

[TOC]

# Section 1: Using Date.prototype.toLocaleString()

The Date.prototype.toLocaleString() method can be used to get the month and date in 2 digit format.

Syntax:
```
dateObj.toLocaleString('default', { month: '2-digit', day: '2-digit' });
```

Example:
```
let date = new Date();
let monthAndDate = date.toLocaleString('default', { month: '2-digit', day: '2-digit' });
console.log(monthAndDate); // Outputs "03/07"
```

# Section 2: Using Date.prototype.toLocaleDateString()

The Date.prototype.toLocaleDateString() method can also be used to get the month and date in 2 digit format.

Syntax:
```
dateObj.toLocaleDateString('default', { month: '2-digit', day: '2-digit' });
```

Example:
```
let date = new Date();
let monthAndDate = date.toLocaleDateString('default', { month: '2-digit', day: '2-digit' });
console.log(monthAndDate); // Outputs "03/07"
```

# Section 3: Using Date.prototype.getMonth() and Date.prototype.getDate()

The Date.prototype.getMonth() and Date.prototype.getDate() methods can also be used to get the month and date in 2 digit format.

Syntax:
```
let month = dateObj.getMonth() + 1; // Add 1 to get the correct month number
let date = dateObj.getDate();
let monthAndDate = (month < 10 ? '0' : '') + month + '/' + (date < 10 ? '0' : '') + date;
```

Example:
```
let date = new Date();
let month = date.getMonth() + 1;
let date = date.getDate();
let monthAndDate = (month < 10 ? '0' : '') + month + '/' + (date < 10 ? '0' : '') + date;
console.log(monthAndDate); // Outputs "03/07"
```

# Section 4: Using Moment.js Library

The Moment.js library can also be used to get the month and date in 2 digit format.

Syntax:
```
let monthAndDate = moment().format('MM/DD');
```

Example:
```
let monthAndDate = moment().format('MM/DD');
console.log(monthAndDate); // Outputs "03/07"
```
