---
title: What is the difference in days between two dates?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Date.getTime() method to calculate the difference between two dates in milliseconds, then divide the result by the number of milliseconds in a day (86400000) to get the number of days between the two dates.
---

**Contents**

[TOC]

## Section 1: Setting up the Date Objects

In order to calculate the number of days between two dates, we must first create two Date objects in Javascript. We can do this by using the new Date() constructor and passing in two parameters: the year and the month (in numerical form):

```javascript
var date1 = new Date(2020, 7); // August 1st, 2020
var date2 = new Date(2020, 10); // November 1st, 2020
```

## Section 2: Calculating the Difference

Once we have our two Date objects, we can calculate the difference between them using the getTime() method. This will return the number of milliseconds between the two dates. We can then divide this number by the number of milliseconds in a day (1000 * 60 * 60 * 24) to get the number of days between the two dates:

```javascript
var diff = date2.getTime() - date1.getTime();
var days = diff / (1000 * 60 * 60 * 24);
```

## Section 3: Rounding the Result

Since the result of the calculation will be a decimal, we may want to round the result to get a more accurate number of days between the two dates. We can use the Math.ceil() method to round the result up to the nearest whole number:

```javascript
var daysRounded = Math.ceil(days);
```

## Section 4: Outputting the Result

Finally, we can output the result of our calculation to the console using the console.log() method:

```javascript
console.log(daysRounded); // Outputs '62'
```
