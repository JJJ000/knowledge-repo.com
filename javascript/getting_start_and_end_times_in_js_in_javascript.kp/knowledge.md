---
title: What is the syntax for finding the beginning and end of the day in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Date object`s getHours(), getMinutes(), getSeconds() methods to get the start and end of the day in JavaScript.
---

**Contents**

[TOC]

# Section 1 - Using Date

The Date object in JavaScript can be used to get the start and end of a day. To get the start of the day, create a Date object for the current day and set the time to 00:00:00. To get the end of the day, create a Date object for the current day and set the time to 23:59:59.

```js
// Get start of day
var startOfDay = new Date();
startOfDay.setHours(0,0,0,0);

// Get end of day
var endOfDay = new Date();
endOfDay.setHours(23,59,59,999);
```

# Section 2 - Using Moment.js

The Moment.js library can be used to get the start and end of a day. To get the start of the day, use the startOf() method with 'day' as the argument. To get the end of the day, use the endOf() method with 'day' as the argument.

```js
// Get start of day
var startOfDay = moment().startOf('day');

// Get end of day
var endOfDay = moment().endOf('day');
```

# Section 3 - Using Lodash

The Lodash library can be used to get the start and end of a day. To get the start of the day, use the startOfDay() method. To get the end of the day, use the endOfDay() method.

```js
// Get start of day
var startOfDay = _.startOfDay(new Date());

// Get end of day
var endOfDay = _.endOfDay(new Date());
```

# Section 4 - Using Native JavaScript

The native JavaScript methods can be used to get the start and end of a day. To get the start of the day, use the getTime() method and set the time to 0. To get the end of the day, use the getTime() method and set the time to 86400000 (24 hours).

```js
// Get start of day
var startOfDay = new Date();
startOfDay.setTime(0);

// Get end of day
var endOfDay = new Date();
endOfDay.setTime(86400000);
```
