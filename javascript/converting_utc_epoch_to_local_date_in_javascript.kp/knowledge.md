---
title: Change a utc epoch time to the corresponding local date and time
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Date constructor to create a Date object from the UTC Epoch time and then use the .toLocaleString() method to get the local date.
---

**Contents**

[TOC]

### Using Date()

The Date() constructor can be used to convert a UTC Epoch timestamp to a local date. The Date() constructor takes a single parameter, which is the UTC Epoch timestamp. The UTC Epoch timestamp is the number of milliseconds that have elapsed since January 1, 1970 00:00:00 UTC.

```
var timestamp = 1590234800000;
var localDate = new Date(timestamp);
console.log(localDate); // Mon May 25 2020 16:00:00 GMT+0800 (Malaysia Time)
```

### Using Moment.js

Moment.js is a popular JavaScript library for working with dates and times. It can be used to convert a UTC Epoch timestamp to a local date.

The moment() constructor takes a single parameter, which is the UTC Epoch timestamp. The UTC Epoch timestamp is the number of milliseconds that have elapsed since January 1, 1970 00:00:00 UTC.

```
var timestamp = 1590234800000;
var localDate = moment(timestamp).format('dddd, MMMM Do YYYY, h:mm:ss a');
console.log(localDate); // Monday, May 25th 2020, 4:00:00 pm
```
