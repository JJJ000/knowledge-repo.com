---
title: Comparing dates and times using moment.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Moment.js can be used to compare dates and times in JavaScript by using the .isBefore(), .isSame(), and .isAfter() functions.
---

**Contents**

[TOC]

## Moment.js

Moment.js is a JavaScript library that helps developers to parse, validate, manipulate, and display dates and times in JavaScript. It is a lightweight library that provides a simple API to allow developers to easily handle date and time operations. Moment.js supports both server-side and client-side operations, making it a great choice for both web and mobile applications.

## Date Time Comparison

Date time comparison in Moment.js can be done in two ways:

1. Using the `isSame()` Method: This method compares two dates and returns true if they are the same, false otherwise.

2. Using the `diff()` Method: This method returns the difference between two dates, in milliseconds. This can be used to compare two dates to determine which date is earlier or later.

## Example

Let's look at an example of how to compare two dates using Moment.js.

```javascript
// Create two moment objects
var date1 = moment("2020-04-01");
var date2 = moment("2020-04-02");
 
// Compare the two dates
if(date1.isSame(date2)) {
    console.log("The dates are the same!");
} else {
    console.log("The dates are not the same!");
}

// Get the difference between the two dates
var diff = date1.diff(date2);

// Print the difference
console.log("The difference between the two dates is: " + diff + " milliseconds");
```

In this example, we create two moment objects for two dates, and then compare them using the `isSame()` method. We also use the `diff()` method to get the difference between the two dates.
