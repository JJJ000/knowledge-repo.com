---
title: Convert a moment.js object to a date object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Moment.js can be used to transform a date string into a Date object in JavaScript.
---

**Contents**

[TOC]

##### Using Moment.js

Using Moment.js, we can easily transform a date string into a date object. This is done by using the `moment()` function.

```js
let dateString = '2020-07-17';
let dateObject = moment(dateString);
```

##### Without Moment.js

It is also possible to transform a date string into a date object without using Moment.js. This can be done by using the `Date()` constructor.

```js
let dateString = '2020-07-17';
let dateObject = new Date(dateString);
```
