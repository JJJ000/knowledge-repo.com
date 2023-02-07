---
title: What is the syntax for increasing a date by a certain number of months in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can add months to a date in JavaScript by using the Date.prototype.setMonth() method.
---

**Contents**

[TOC]

### Using Date.prototype.setMonth()

The `Date.prototype.setMonth()` method can be used to add months to a date in JavaScript.

Syntax:
```
dateObj.setMonth(monthValue[, dayValue])
```

Parameters:
- **monthValue**: An integer between 0 and 11 representing the month. 0 corresponds to January, 1 to February, and so on.
- **dayValue**: An integer between 1 and 31 representing the day of the month.

Example:
```
let date = new Date(2020, 0, 15);
date.setMonth(date.getMonth() + 2);
console.log(date);  // 2020-02-15T00:00:00.000Z
```

### Using Date.prototype.setFullYear()

The `Date.prototype.setFullYear()` method can also be used to add months to a date in JavaScript.

Syntax:
```
dateObj.setFullYear(yearValue[, monthValue[, dayValue]])
```

Parameters:
- **yearValue**: An integer representing the year.
- **monthValue**: An integer between 0 and 11 representing the month. 0 corresponds to January, 1 to February, and so on.
- **dayValue**: An integer between 1 and 31 representing the day of the month.

Example:
```
let date = new Date(2020, 0, 15);
date.setFullYear(date.getFullYear(), date.getMonth() + 2, date.getDate());
console.log(date);  // 2020-02-15T00:00:00.000Z
```
