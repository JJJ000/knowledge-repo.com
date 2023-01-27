---
title: What is the syntax for formatting a date in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can format a date in JavaScript using the Date.prototype.toLocaleString() method.
---

**Contents**

[TOC]

### Using the Date Constructor

The Date constructor can be used to create a Date object in JavaScript. The constructor takes a number of arguments to specify the date, and the date can be formatted by passing the Date object to the `toLocaleDateString()` method. 

```javascript
// Create a Date object with the constructor
let date = new Date(2020, 11, 24); 

// Format the date with toLocaleDateString()
let formattedDate = date.toLocaleDateString(); 

console.log(formattedDate); // Outputs "12/24/2020"
```

### Using an External Library

An external library such as Moment.js can be used to format a date. Moment.js is a popular library for working with dates and times in JavaScript. 

To use Moment.js, the library must first be included in the project. This can be done by using a CDN or by downloading the library and including it in the project. 

Once the library is included, a Date object can be passed to the `format()` method of the Moment object. This method takes a formatting string as an argument and returns the formatted date. 

```javascript
// Include Moment.js
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.27.0/moment.min.js"></script>

// Create a Date object
let date = new Date(2020, 11, 24); 

// Format the date with Moment.js
let formattedDate = moment(date).format("MM/DD/YYYY"); 

console.log(formattedDate); // Outputs "12/24/2020"
```
