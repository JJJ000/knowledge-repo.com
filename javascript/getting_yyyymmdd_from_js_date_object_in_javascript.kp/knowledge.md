---
title: How can I obtain a string in yyyymmdd format from a JavaScript date object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can get a string in YYYYMMDD format from a JS date object using the .toISOString() method.
---

**Contents**

[TOC]

### Using Date.prototype.toISOString()

The `toISOString()` method returns a string in simplified extended ISO format (ISO 8601), which is always 24 or 27 characters long (YYYY-MM-DDTHH:mm:ss.sssZ or ±YYYYYY-MM-DDTHH:mm:ss.sssZ, respectively).

```javascript
var date = new Date();
var yyyymmdd = date.toISOString().slice(0,10).replace(/-/g,"");
```

### Using Date.prototype.toLocaleDateString()

The `toLocaleDateString()` method returns a string with a language sensitive representation of the date portion of the Date.

```javascript
var date = new Date();
var yyyymmdd = date.toLocaleDateString().replace(/\//g,"");
```

### Using Date.prototype.getFullYear(), Date.prototype.getMonth() and Date.prototype.getDate()

The `getFullYear()`, `getMonth()` and `getDate()` methods returns the year, month and date respectively.

```javascript
var date = new Date();
var yyyy = date.getFullYear();
var mm = date.getMonth() + 1; // getMonth() is zero-based
var dd  = date.getDate();

var yyyymmdd = yyyy + '' + (mm[1]?mm:"0"+mm[0]) + '' + (dd[1]?dd:"0"+dd[0]); // padding
```

### Using Intl.DateTimeFormat()

The `Intl.DateTimeFormat()` method returns a new `Intl.DateTimeFormat` object.

```javascript
var date = new Date();
var options = { year: 'numeric', month: '2-digit', day: '2-digit' };
var yyyymmdd = new Intl.DateTimeFormat('en-US', options).format(date).replace(/\//g,"");
```
