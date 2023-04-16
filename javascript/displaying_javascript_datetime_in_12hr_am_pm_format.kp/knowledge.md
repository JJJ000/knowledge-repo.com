---
title: What is the best way to show a JavaScript date and time in 12 hour am/pm format?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the toLocaleString() method with the `en-US` locale and the `hmm a` options to display the JavaScript DateTime in 12 hour AM/PM format.
---

**Contents**

[TOC]

### Using toLocaleTimeString

The `toLocaleTimeString()` method can be used to convert the JavaScript Date object to a 12 hour AM/PM format. This method takes two arguments, a locale and an options object. The locale argument is used to set the language, and the options object can be used to customize the output.

```javascript
let date = new Date();
let options = {
    hour: '2-digit',
    minute: '2-digit',
    hour12: true
};
let timeString = date.toLocaleTimeString('en-US', options);
console.log(timeString);
// Outputs: "11:22 PM"
```

### Using toString

The `toString()` method can also be used to convert the JavaScript Date object to a 12 hour AM/PM format. This method takes no arguments and returns a string representation of the date in the local timezone.

```javascript
let date = new Date();
let timeString = date.toString();
console.log(timeString);
// Outputs: "Tue Mar 16 2021 11:22:35 GMT-0400 (Eastern Daylight Time)"
```

The returned string can be further parsed to extract the time in 12 hour AM/PM format.

### Using Moment.js

The Moment.js library can also be used to convert the JavaScript Date object to a 12 hour AM/PM format. Moment.js is a popular JavaScript library for manipulating dates and times.

```javascript
let date = new Date();
let timeString = moment(date).format('h:mm A');
console.log(timeString);
// Outputs: "11:22 PM"
```
