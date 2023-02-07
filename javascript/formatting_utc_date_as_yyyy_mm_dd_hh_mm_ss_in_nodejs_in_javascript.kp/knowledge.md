---
title: What is the syntax for formatting a utc date as a "yyyy-mm-dd hhmmss" string using nodejs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `toISOString()` method on a Date object to format it as a `YYYY-MM-DD hhmmss` string.
---

**Contents**

[TOC]

### Using Date()

The following code uses the Date() constructor to format a UTC date as a `YYYY-MM-DD hh:mm:ss` string.

```javascript
let date = new Date();
let utcDate = date.toISOString();
let formattedDate = utcDate.substring(0, 19).replace('T', ' ');
console.log(formattedDate); // Outputs: YYYY-MM-DD hh:mm:ss
```

### Using Moment.js

The following code uses the Moment.js library to format a UTC date as a `YYYY-MM-DD hh:mm:ss` string.

```javascript
let date = moment.utc();
let formattedDate = date.format('YYYY-MM-DD HH:mm:ss');
console.log(formattedDate); // Outputs: YYYY-MM-DD hh:mm:ss
```

### Using Intl.DateTimeFormat

The following code uses the Intl.DateTimeFormat constructor to format a UTC date as a `YYYY-MM-DD hh:mm:ss` string.

```javascript
let date = new Date();
let options = {
    year: 'numeric',
    month: '2-digit',
    day: '2-digit',
    hour: '2-digit',
    minute: '2-digit',
    second: '2-digit'
};
let formattedDate = new Intl.DateTimeFormat('en-US', options).format(date);
console.log(formattedDate); // Outputs: YYYY-MM-DD hh:mm:ss
```
