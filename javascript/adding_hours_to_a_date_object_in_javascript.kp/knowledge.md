---
title: What is the process for increasing the time of a date object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can add hours to a Date object in Javascript by using the Date.prototype.setHours() method.
---

**Contents**

[TOC]

### Using the Date.setHours() Method

The `Date.setHours()` method can be used to add hours to a Date object. This method takes two parameters, the hour and the minutes, and sets the Date object to the specified hour and minutes.

The following example adds three hours to the current Date object:

```javascript
let date = new Date();
date.setHours(date.getHours() + 3);
```

### Using the Date.getTime() Method

The `Date.getTime()` method can be used to add hours to a Date object. This method returns the number of milliseconds since 1 January 1970 00:00:00 UTC.

The following example adds three hours to the current Date object:

```javascript
let date = new Date();
let newDate = new Date(date.getTime() + (3 * 60 * 60 * 1000));
```

### Using the Date.now() Method

The `Date.now()` method can be used to add hours to a Date object. This method returns the number of milliseconds since 1 January 1970 00:00:00 UTC.

The following example adds three hours to the current Date object:

```javascript
let date = new Date(Date.now() + (3 * 60 * 60 * 1000));
```

### Using the Date.prototype.setTime() Method

The `Date.prototype.setTime()` method can be used to add hours to a Date object. This method sets the Date object to the specified number of milliseconds since 1 January 1970 00:00:00 UTC.

The following example adds three hours to the current Date object:

```javascript
let date = new Date();
date.setTime(date.getTime() + (3 * 60 * 60 * 1000));
```
