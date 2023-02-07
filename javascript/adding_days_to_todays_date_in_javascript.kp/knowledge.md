---
title: What is the procedure for calculating a future date given a certain number of days from today?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can add number of days to today`s date in Javascript by using the Date object`s setDate() method.
---

**Contents**

[TOC]

## Section 1: Create a Date object

In order to add a number of days to today's date, we must first create a `Date` object. This can be done by calling the `Date` constructor with no arguments.

```
let today = new Date();
```

## Section 2: Calculate the Number of Milliseconds

Since the `Date` constructor takes milliseconds as its argument, we must calculate the number of milliseconds for the number of days we want to add. This can be done by multiplying the number of days by 86400000, which is the number of milliseconds in a day.

```
let numDays = 7;
let numMilliseconds = numDays * 86400000;
```

## Section 3: Add the Number of Milliseconds to the Date Object

Once we have our `Date` object and the number of milliseconds, we can add the two together by calling the `setTime()` method on the `Date` object. This will set the date to the new value by adding the number of milliseconds to the current date.

```
today.setTime(today.getTime() + numMilliseconds);
```

## Section 4: Output the Date

Finally, we can output the new date by calling the `toDateString()` method on the `Date` object.

```
console.log(today.toDateString());
```
