---
title: What is the procedure for increasing the number of days in a date?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can add days to a date in JavaScript by using the Date.prototype.setDate() method.
---

**Contents**

[TOC]

1. Using the Date Constructor 

The Date constructor takes three parameters, year, month and day. To add days to the date, simply increment the day parameter by the desired number of days.

```
let date = new Date(2020, 3, 15);
date.setDate(date.getDate() + 7);
console.log(date); // Mon Apr 22 2020 00:00:00 GMT+0530 (India Standard Time)
```

2. Using the setDate() Method 

The setDate() method sets the day of the month for a specified date according to local time. It can be used to add days to the date by passing a parameter that is greater than the current day of the month.

```
let date = new Date(2020, 3, 15);
date.setDate(date.getDate() + 7);
console.log(date); // Mon Apr 22 2020 00:00:00 GMT+0530 (India Standard Time)
```

3. Using the getTime() and setTime() Methods 

The getTime() method returns the number of milliseconds since January 1, 1970, 00:00:00 UTC. We can use this method to add days to the date by multiplying the number of days by the number of milliseconds in a day (86400000).

```
let date = new Date(2020, 3, 15);
let newDate = new Date(date.getTime() + (7 * 86400000));
console.log(newDate); // Mon Apr 22 2020 00:00:00 GMT+0530 (India Standard Time)
```

4. Using the Moment.js Library 

The Moment.js library is a popular JavaScript library for working with dates and times. It can be used to add days to a date by using the add() method.

```
let date = moment('2020-03-15');
date.add(7, 'days');
console.log(date.format('YYYY-MM-DD')); // 2020-04-22
```
