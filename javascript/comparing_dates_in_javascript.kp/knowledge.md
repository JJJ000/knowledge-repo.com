---
title: Determine which of two dates is earlier or later using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The two dates can be compared using the Date.prototype.getTime() method, which returns the number of milliseconds since January 1, 1970 for each date.
---

**Contents**

[TOC]

#1 Using Date.parse()

The Date.parse() method parses a date string and returns the number of milliseconds since January 1, 1970. This method can be used to compare two dates by subtracting the two millisecond values.

```javascript
let date1 = Date.parse("12/31/2019");
let date2 = Date.parse("1/1/2020");

let difference = date2 - date1;

if (difference > 0) {
  console.log("date2 is after date1");
} else if (difference < 0) {
  console.log("date1 is after date2");
} else {
  console.log("date1 and date2 are equal");
}
```

#2 Using Date.getTime()

The Date.getTime() method returns the number of milliseconds since January 1, 1970. This method can be used to compare two dates by subtracting the two millisecond values.

```javascript
let date1 = new Date("12/31/2019").getTime();
let date2 = new Date("1/1/2020").getTime();

let difference = date2 - date1;

if (difference > 0) {
  console.log("date2 is after date1");
} else if (difference < 0) {
  console.log("date1 is after date2");
} else {
  console.log("date1 and date2 are equal");
}
```
