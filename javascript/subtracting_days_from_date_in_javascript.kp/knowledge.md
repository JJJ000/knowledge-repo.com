---
title: What is the process for subtracting days from a regular date?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Subtract the number of days from the Date object using the Date.setDate() method.
---

**Contents**

[TOC]

1. Using the Date Constructor 

```javascript
let date = new Date("2020-02-01");
let daysToSubtract = 5;

date.setDate(date.getDate() - daysToSubtract);
console.log(date);
```

2. Using Moment.js

```javascript
let date = moment("2020-02-01");
let daysToSubtract = 5;

date.subtract(daysToSubtract, 'days');
console.log(date.format("YYYY-MM-DD"));
```

3. Using Date-fns

```javascript
let date = new Date("2020-02-01");
let daysToSubtract = 5;

let newDate = subDays(date, daysToSubtract);
console.log(format(newDate, "yyyy-MM-dd"));
```

4. Using Lodash

```javascript
let date = new Date("2020-02-01");
let daysToSubtract = 5;

let newDate = _.subtract(date, daysToSubtract * 24 * 60 * 60 * 1000);
console.log(format(newDate, "yyyy-MM-dd"));
```
