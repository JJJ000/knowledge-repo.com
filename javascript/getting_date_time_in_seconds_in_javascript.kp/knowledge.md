---
title: What is the current date and/or time in seconds?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The current date and time in seconds can be obtained using the Date.now() method.
---

**Contents**

[TOC]

### Using Date.now()

The Date.now() method returns the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC. To get the current date in seconds, you can divide the result of Date.now() by 1000.

```javascript
var currentDateInSeconds = Date.now() / 1000;
```

### Using getTime()

The getTime() method returns the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC. To get the current date in seconds, you can divide the result of getTime() by 1000.

```javascript
var currentDateInSeconds = new Date().getTime() / 1000;
```

### Using toUTCString()

The toUTCString() method returns a string representing the date as a UTC date. To get the current date in seconds, you can convert the result of toUTCString() to a Date object and divide the result of getTime() by 1000.

```javascript
var currentDateInSeconds = new Date(Date.UTC(new Date().toUTCString())).getTime() / 1000;
```

### Using toISOString()

The toISOString() method returns a string representing the date as an ISO date. To get the current date in seconds, you can convert the result of toISOString() to a Date object and divide the result of getTime() by 1000.

```javascript
var currentDateInSeconds = new Date(Date.parse(new Date().toISOString())).getTime() / 1000;
```
