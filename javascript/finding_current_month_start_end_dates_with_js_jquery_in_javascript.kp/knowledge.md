---
title: Find the start and end dates of the current month using JavaScript or jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Using JavaScript, the first and last date of the current month can be obtained using the Date object`s getDate(), getMonth(), and getFullYear() methods.
---

**Contents**

[TOC]

# Javascript

## Date Object
```
var date = new Date();
var firstDay = new Date(date.getFullYear(), date.getMonth(), 1);
var lastDay = new Date(date.getFullYear(), date.getMonth() + 1, 0);

console.log(firstDay);
console.log(lastDay);
```

## Moment.js
```
var firstDay = moment().startOf('month').format('YYYY-MM-DD');
var lastDay = moment().endOf('month').format('YYYY-MM-DD');

console.log(firstDay);
console.log(lastDay);
```

# jQuery

## Datepicker
```
var firstDay = $('#datepicker').datepicker('option', 'firstDay');
var lastDay = $('#datepicker').datepicker('option', 'lastDay');

console.log(firstDay);
console.log(lastDay);
```

## Moment.js
```
var firstDay = moment().startOf('month').format('YYYY-MM-DD');
var lastDay = moment().endOf('month').format('YYYY-MM-DD');

console.log(firstDay);
console.log(lastDay);
```
