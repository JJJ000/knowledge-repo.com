---
title: Change a unix timestamp into a readable time format using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can convert a Unix timestamp to time in JavaScript by using the Date constructor and passing in the timestamp as an argument.
---

**Contents**

[TOC]

### Method 1: Using Date Constructor

```javascript
let unix_timestamp = 1545730073;

// Create a new JavaScript Date object based on the timestamp
// multiplied by 1000 so that the argument is in milliseconds, not seconds.
let date = new Date(unix_timestamp*1000);

// Hours part from the timestamp
let hours = date.getHours();

// Minutes part from the timestamp
let minutes = "0" + date.getMinutes();

// Seconds part from the timestamp
let seconds = "0" + date.getSeconds();

// Will display time in 10:30:23 format
let formattedTime = hours + ':' + minutes.substr(-2) + ':' + seconds.substr(-2);

console.log(formattedTime);
```

### Method 2: Using Moment.js

```javascript
let unix_timestamp = 1545730073;

// Create a new date from the timestamp
let date = moment.unix(unix_timestamp);

// Format the date
let formattedTime = date.format("HH:mm:ss");

console.log(formattedTime);
```
