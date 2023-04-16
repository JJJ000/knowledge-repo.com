---
title: What is the code to retrieve the current date in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get the current date in JavaScript by using the Date() constructor.
---

**Contents**

[TOC]

# Section 1 - Using Date()

The most common way to get the current date in JavaScript is by using the `Date()` constructor. This constructor takes no arguments and returns a `Date` object representing the current date and time.

```javascript
const currentDate = new Date();
```

# Section 2 - Using getFullYear()

Once you have a `Date` object, you can use the `getFullYear()` method to get the current year. 

```javascript
const currentYear = currentDate.getFullYear();
```

# Section 3 - Using getMonth()

You can also use the `getMonth()` method to get the current month. This method returns a number from 0-11, so you may need to add 1 to get the month as it appears in a date.

```javascript
const currentMonth = currentDate.getMonth() + 1;
```

# Section 4 - Using getDate()

Finally, you can use the `getDate()` method to get the current day of the month.

```javascript
const currentDay = currentDate.getDate();
```
