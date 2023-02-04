---
title: Change utc date time to the corresponding local date time
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the Date.prototype.getTimezoneOffset() method to convert UTC date time to local date time in Javascript.
---

**Contents**

[TOC]

## Section 1: Introduction

UTC (Coordinated Universal Time) is a standard time reference used to calculate local time in different regions. It is the primary time standard by which the world regulates clocks and time. UTC is often used in programming, especially when dealing with date and time values. In JavaScript, it is possible to convert UTC date time to local date time using the Date object and its methods.

## Section 2: Date Constructor

The Date constructor is the main tool used to convert UTC date time to local date time. It is a built-in JavaScript object that can be used to create a date object from a given string or integer. The Date constructor can be used to create a date object from a UTC date time string. The syntax for the Date constructor is as follows:

```
var date = new Date(dateString);
```

Where `dateString` is a string representing a valid UTC date time. The Date constructor will return a date object with the specified UTC date time.

## Section 3: getTimezoneOffset Method

The getTimezoneOffset method is a Date object method that returns the time difference between UTC and the local timezone in minutes. The syntax for the getTimezoneOffset method is as follows:

```
date.getTimezoneOffset();
```

Where `date` is a Date object. The getTimezoneOffset method will return an integer representing the time difference between UTC and the local timezone in minutes.

## Section 4: Date.prototype.getTime Method

The Date.prototype.getTime method is a Date object method that returns the number of milliseconds since the Unix epoch (January 1, 1970). The syntax for the Date.prototype.getTime method is as follows:

```
date.getTime();
```

Where `date` is a Date object. The Date.prototype.getTime method will return an integer representing the number of milliseconds since the Unix epoch.

By combining the Date constructor, getTimezoneOffset method, and Date.prototype.getTime method, it is possible to convert UTC date time to local date time in JavaScript.
