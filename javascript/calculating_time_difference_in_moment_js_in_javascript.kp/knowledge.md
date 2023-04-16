---
title: Find the number of hours between two dates using moment js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Moment.js can be used to calculate the difference between two dates in hours using the .diff() method.
---

**Contents**

[TOC]

### Section 1: 

Moment.js

### Section 2: 

Calculating the Difference

Moment.js provides a function to calculate the difference between two dates. This function is called `diff()`. It takes two parameters, which are the two dates that you want to compare. The `diff()` function will return the difference between the two dates in milliseconds.

### Section 3: 

Converting to Hours

Once you have the difference in milliseconds, you can easily convert it to hours by dividing it by the number of milliseconds in an hour (3,600,000).

### Section 4: 

Example

For example, if you wanted to calculate the difference between two dates, you could use the following code:

```
var date1 = moment("2020-01-01");
var date2 = moment("2020-01-02");

var diffInMilliseconds = date1.diff(date2);

var diffInHours = diffInMilliseconds / 3600000;
```

The result of this code would be 24 hours.
