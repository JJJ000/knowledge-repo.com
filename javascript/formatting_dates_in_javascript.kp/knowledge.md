---
title: Convert JavaScript date to yyyy-mm-dd format
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the built-in Date.prototype.toISOString() method to format a JavaScript date as yyyy-mm-dd.
---

**Contents**

[TOC]

# Solution 1

Using `toISOString()`:

```javascript
var date = new Date();
var dateString = date.toISOString().substring(0, 10);
```

# Solution 2

Using `toLocaleDateString()`:

```javascript
var date = new Date();
var dateString = date.toLocaleDateString('en-US', {
  year: 'numeric',
  month: '2-digit',
  day: '2-digit'
});
```

# Solution 3

Using `getFullYear()`, `getMonth()` and `getDate()`:

```javascript
var date = new Date();
var year = date.getFullYear();
var month = (1 + date.getMonth()).toString().padStart(2, '0');
var day = date.getDate().toString().padStart(2, '0');
var dateString = year + '-' + month + '-' + day;
```

# Solution 4

Using `toJSON()`:

```javascript
var date = new Date();
var dateString = date.toJSON().substring(0, 10);
```
