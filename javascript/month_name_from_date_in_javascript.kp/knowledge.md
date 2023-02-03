---
title: Retrieve the month from a given date
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The month name can be retrieved from a Date object in Javascript using the getMonth() method.
---

**Contents**

[TOC]

1. Getting the Month Name from a Date Object
------------------------------------------------
Using the `getMonth()` method of the Date object, you can get the numerical value of the month from 0-11. To get the name of the month, you can use an array of month names and access the element at the numerical index.

```javascript
const monthNames = ["January", "February", "March", "April", "May", "June",
  "July", "August", "September", "October", "November", "December"
];

let d = new Date();
let monthIndex = d.getMonth();
let monthName = monthNames[monthIndex];

console.log(monthName); // Outputs "August"
```

2. Getting the Month Name from a String
------------------------------------------------
If you have a string representing a date, you can use the `Date.parse()` method to convert it to a Date object and then use the `getMonth()` method to get the numerical value of the month. From there, you can use the same array of month names to get the name of the month.

```javascript
const monthNames = ["January", "February", "March", "April", "May", "June",
  "July", "August", "September", "October", "November", "December"
];

let dateString = "08/14/2020";
let d = Date.parse(dateString);
let monthIndex = d.getMonth();
let monthName = monthNames[monthIndex];

console.log(monthName); // Outputs "August"
```

3. Using a Library
------------------------------------------------
If you don't want to manually create an array of month names and access the element at the numerical index, you can use a library such as Moment.js to get the month name from a Date object or a string.

```javascript
let d = new Date();
let monthName = moment(d).format('MMMM');

console.log(monthName); // Outputs "August"
```

4. Using Intl.DateTimeFormat
------------------------------------------------
Another option is to use the `Intl.DateTimeFormat` object to get the month name from a Date object.

```javascript
let d = new Date();
let monthName = new Intl.DateTimeFormat('en-US', {month: 'long'}).format(d);

console.log(monthName); // Outputs "August"
```
