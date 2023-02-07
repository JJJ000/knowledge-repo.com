---
title: What is the syntax to extract the year, month, and day from a date object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the getFullYear(), getMonth(), and getDate() methods of the Date object to get the year, month, and day, respectively.
---

**Contents**

[TOC]

#### Using the getFullYear() Method

The `getFullYear()` method is used to get the year of a given date object.

```javascript
let d = new Date();
let year = d.getFullYear();

console.log(year); // Outputs the current year
```

#### Using the getMonth() Method

The `getMonth()` method is used to get the month of a given date object.

```javascript
let d = new Date();
let month = d.getMonth();

console.log(month); // Outputs the current month (January is 0, February is 1, etc.)
```

#### Using the getDate() Method

The `getDate()` method is used to get the day of a given date object.

```javascript
let d = new Date();
let day = d.getDate();

console.log(day); // Outputs the current day
```

#### Using the toLocaleDateString() Method

The `toLocaleDateString()` method is used to get the date in the local time zone.

```javascript
let d = new Date();
let date = d.toLocaleDateString();

console.log(date); // Outputs the current date in local time zone
```
