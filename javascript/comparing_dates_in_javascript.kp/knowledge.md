---
title: Comparing only the date portion of two dates in JavaScript without taking the time into account
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the Date.prototype.toDateString() method to compare only the date part without the time.
---

**Contents**

[TOC]

1. Using Moment.js
------------------------
Moment.js is a lightweight JavaScript date library for parsing, validating, manipulating, and formatting dates. It is widely used and provides an easy way to compare dates without considering the time. 

To compare dates using Moment.js, you can use the `isSame()` function. This function takes two parameters and returns a Boolean value indicating if the two dates are the same.

```
var date1 = moment("2018-05-15");
var date2 = moment("2018-05-16");

if (date1.isSame(date2)) {
    console.log("The dates are the same");
} else {
    console.log("The dates are different");
}
```

2. Using Date.prototype.getFullYear()
------------------------
The Date.prototype.getFullYear() method can be used to compare dates without considering the time. This method returns the year in the specified date according to local time.

To compare dates using this method, you can create two Date objects and compare the year returned by the getFullYear() method.

```
var date1 = new Date("2018-05-15");
var date2 = new Date("2018-05-16");

if (date1.getFullYear() === date2.getFullYear()) {
    console.log("The dates are the same");
} else {
    console.log("The dates are different");
}
```
