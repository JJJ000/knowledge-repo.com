---
title: Converting a string into a date in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Date.parse() method to parse a string to a date in JavaScript.
---

**Contents**

[TOC]

### Using the Date Constructor
The Date constructor can be used to parse a string to a date.

Syntax:

`var date = new Date(dateString);`

Example:

`var date = new Date("2020-04-13");`

### Using the Date.parse() Method
The Date.parse() method can also be used to parse a string to a date.

Syntax:

`var date = Date.parse(dateString);`

Example:

`var date = Date.parse("2020-04-13");`

### Using the Date.UTC() Method
The Date.UTC() method can be used to parse a string to a date in UTC time.

Syntax:

`var date = Date.UTC(year, month, day);`

Example:

`var date = Date.UTC(2020, 3, 13);`

### Using the Moment.js Library
The Moment.js library can also be used to parse a string to a date.

Syntax:

`var date = moment(dateString);`

Example:

`var date = moment("2020-04-13");`
