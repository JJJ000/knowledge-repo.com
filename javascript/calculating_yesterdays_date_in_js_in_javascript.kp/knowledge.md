---
title: Determine the date of the previous day in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yesterday`s date can be calculated using the Date object`s built-in getDate() method, which returns the day of the month minus one.
---

**Contents**

[TOC]

# Section 1: Calculate Date

```javascript
var yesterday = new Date();
yesterday.setDate(yesterday.getDate() - 1);
```

# Section 2: Format Date

```javascript
var dd = yesterday.getDate();
var mm = yesterday.getMonth() + 1;
var yyyy = yesterday.getFullYear();

if (dd < 10) {
  dd = '0' + dd;
} 

if (mm < 10) {
  mm = '0' + mm;
} 

yesterday = mm + '/' + dd + '/' + yyyy;
```

# Section 3: Output Date

```javascript
console.log(yesterday);
```

# Section 4: Result

The date yesterday is printed in the console as `mm/dd/yyyy`, e.g. `07/17/2020`.
