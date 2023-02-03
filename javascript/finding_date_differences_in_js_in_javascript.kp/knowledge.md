---
title: How do I calculate the amount of time between two dates in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can get the difference between two dates in JavaScript by subtracting one date from the other and getting the difference in milliseconds.
---

**Contents**

[TOC]

**Section 1: Getting Two Dates**

To get two dates in JavaScript, you can use the Date constructor. This constructor takes a string representing the date as an argument and returns a Date object.

For example:

```javascript
let date1 = new Date("June 1, 2020");
let date2 = new Date("June 15, 2020");
```

**Section 2: Calculating the Difference**

To calculate the difference between two dates, you can use the Date.getTime() method. This method returns the number of milliseconds since January 1, 1970.

For example:

```javascript
let difference = date2.getTime() - date1.getTime();
```

**Section 3: Converting to Days**

To convert the difference to days, you can divide the difference by the number of milliseconds in a day (1000 * 60 * 60 * 24).

For example:

```javascript
let days = difference / (1000 * 60 * 60 * 24);
```

**Section 4: Rounding**

To round the result to the nearest integer, you can use the Math.round() method.

For example:

```javascript
let days = Math.round(days);
```
