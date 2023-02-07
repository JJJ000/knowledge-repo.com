---
title: What is the best way to format time since a certain point (e.g. "4 minutes ago") in a manner similar to stack exchange sites?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Date.prototype.toLocaleString() method with the `relative` option to format time since a given timestamp in Javascript.
---

**Contents**

[TOC]

1. **Using Moment.js**

Moment.js is a lightweight JavaScript library that allows you to easily format dates and times. To format a time since xxx e.g. “4 minutes ago”, you can use the `fromNow()` method.

```javascript
var time = moment().subtract(4, 'minutes').fromNow();
console.log(time); // 4 minutes ago
```

2. **Using Date.now()**

You can also use the `Date.now()` method to get the current timestamp and then subtract the desired amount of minutes to get the timestamp of the desired time.

```javascript
var now = Date.now(); 
var fourMinutesAgo = now - (4 * 60 * 1000); // 4 minutes in milliseconds
var time = new Date(fourMinutesAgo).toLocaleString();
console.log(time); // 4 minutes ago
```

3. **Using Vanilla JavaScript**

You can also use the `Date()` constructor to get the current timestamp and then subtract the desired amount of minutes to get the timestamp of the desired time.

```javascript
var now = new Date(); 
var fourMinutesAgo = now - (4 * 60 * 1000); // 4 minutes in milliseconds
var time = new Date(fourMinutesAgo).toLocaleString();
console.log(time); // 4 minutes ago
```

4. **Using Date-fns**

Date-fns is another popular library for formatting dates and times. To format a time since xxx e.g. “4 minutes ago”, you can use the `distanceInWordsToNow()` method.

```javascript
var fourMinutesAgo = new Date(Date.now() - (4 * 60 * 1000)); // 4 minutes in milliseconds
var time = formatDistanceToNow(fourMinutesAgo);
console.log(time); // 4 minutes ago
```
