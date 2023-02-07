---
title: What is the JavaScript code to get the number of milliseconds since the unix epoch?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can get the time in milliseconds since the unix epoch in Javascript by using the Date.now() method.
---

**Contents**

[TOC]

### Using Date.now()

The `Date.now()` method returns the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC.

```javascript
let millisecondsSinceEpoch = Date.now();
```

### Using getTime()

The `getTime()` method of the `Date` object returns the number of milliseconds since the Unix Epoch.

```javascript
let date = new Date();
let millisecondsSinceEpoch = date.getTime();
```

### Using valueOf()

The `valueOf()` method of the `Date` object returns the primitive value of the `Date` object which is the number of milliseconds since the Unix Epoch.

```javascript
let date = new Date();
let millisecondsSinceEpoch = date.valueOf();
```

### Using toUTCString()

The `toUTCString()` method of the `Date` object returns a string representing the date as a UTC string. This can be converted to a number of milliseconds since the Unix Epoch by subtracting the UTC offset from the current time.

```javascript
let date = new Date();
let millisecondsSinceEpoch = date.toUTCString() - date.getTimezoneOffset() * 60000;
```
