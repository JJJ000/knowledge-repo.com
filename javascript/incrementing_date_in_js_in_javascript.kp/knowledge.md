---
title: Adding a day to a date in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can increment a date in JavaScript by adding the desired number of milliseconds to the current date using the Date.now() method.
---

**Contents**

[TOC]

**Using the Date Object**

The Date object in JavaScript can be used to manipulate and increment dates. To increment a date, you can use the `setDate()` method. The `setDate()` method sets the day of the month for a specified date according to universal time. 

Syntax:
`dateObj.setDate(dayValue)`

Example:

```javascript
let date = new Date();
date.setDate(date.getDate() + 7); // Increment date by 7 days
```

**Using Moment.js**

Moment.js is a popular JavaScript library for working with dates and times. It provides a simple API for manipulating dates and times. To increment a date, you can use the `add()` method.

Syntax:
`moment().add(value, unit)`

Example:

```javascript
let date = moment();
date.add(7, 'days'); // Increment date by 7 days
```
